---
tags: arqcomp
---

Processos são instâncias de um programa em execução, que possuem um espaço de endereçamento lógico, contadores de programa, registradores e variáveis, isto é, entrada, saída e estado. 

> Vale salientar a diferença entre processo e programa, o programa é uma série de instruções modeladas em um ou vários arquivos de código, o processo é a execução desse programa, o programa é a receita, o processo é o preparo.

Vale a pena pensar que por conta da **multiprogramação**, cada processo tem uma CPU **virtual**, embora não seja tecnicamente correto. O computador é capaz de manter vários processos vivos na memória, e a CPU de executar cada um deles por um certo tempo, atualizar os contadores e trocar de processo, existe um certo **pseudo**paralelismo envolvido.

#### Criação de Processos

Em sistemas muito simples, citando o exemplo dos embarcados em microondas por exemplo, é possível ter todos os processos que poderão ser utilizados quando o sistema for ligado. Em sistemas mais complexos, com interação com o usuário, Existem 4 cenários principais para a criação de novos processos:

- Inicialização do Sistema
- Chamadas de sistema por parte de um processo para criação de novos processos filhos
- Solicitação do usuário para criar novo processo.
- Início de uma tarefa em lote *(exclusivo para sistemas em lote)*.

Processos que executam em segundo plano, aguardando algum evento para serem executados, são chamados de **daemons**, alguns exemplos são: o processo que aguarda para notificar a chegada de um novo e-mail, o que está aguardando uma nova solicitação de página web para buscar a retorná-la.

#### Término de Processos

Como nem tudo dura pra sempre, processos, uma vez criados e tendo seu trabalho concluído, (ou algum erro detectado), se encerram. Temos 4 motivos principais para o encerramento dos processos:

- Saída normal (voluntária)
- Erro fatal (involuntária)
- Saída por erro (voluntária)
- Morte por outro processo (involuntária)

Um processo, uma vez tendo terminado seu trabalho, executa uma chamada para o sistema operacional como uma criança que chama sua mãe para limpar sua bundinha no banheiro. No UNIX a chamada se chama `exit`. 
Um erro fatal é quando, por exemplo, se deseja compilar um arquivo que não existe, nesse caso, o compilador graciosamente anuncia que o arquivo indicado não existe, e se encerra. Em programas baseados em tela, geralmente não se encerram, apenas indicam ao usuário para que dê os dados corretamente.
O terceiro motivo é um erro causado pelo processo, em decorrência de um erro de programa, referenciar endereços inválidos e dividir por zero são exemplos de erros de programa.
O quarto motivo é a morte por outro processo, que pode invocar uma [[Chamadas de Sistema]] `kill` para matar o processo indicado, obviamente é necessário possuir a permissão para matar o processo indicado.

#### Hierarquia de Processos

Como dito na seção de criação de processos, um processo pode criar vários filhos, mas  ele somente tem um pai, essa estrutura acaba se tornando uma árvore de processos, onde cada processo possui um pai, filhos e descendentes. No UNIX, um processo e todos os seus descendentes formam um **grupo de processos**, quando um usuário envia, por exemplo, um sinal do teclado, o sinal é entregue a **todos os membros do grupo de processos associados ao teclado**, que podem decidir tomar alguma ação, ignorá-lo ou tomar alguma ação predefinida como, por exemplo, ser morto pelo sinal (Alt F4).

No UNIX, ao inicializar-se o sistema, um único processo é executado, o init, que por sua vez lê um arquivo que diz quantos terminais existem, então, ele se bifurca em um processo para cada terminal, que por sua vez aguardam comandos que podem iniciar novos processos e assim por diante.

#### Estados de Processos

Processos possuem estados dentro do sistema, nenhum processo é executado indefinidamente, existem restrições e condições para que ele seja executado, além de tempo de CPU que é dividido irmãmente entre os processos pelo [[Escalonamento]], um processo que, por exemplo, busca algum texto no arquivo, pode somente buscar esse texto quando o arquivo estiver disponível para ser buscado. Nesse caso, o processo fica **bloqueado** até que sua entrada esteja disponível. Outro motivo para o bloqueio de um processo, é quando a CPU decidiu que ele ocupou tempo o suficiente de CPU e passa a executar outro processo no lugar, nesse caso, o processo, conceitualmente pronto e executável, fica bloqueado até que tenha a oportunidade de rodar novamente. Em geral, existem três estados:

1. Executando (Realmente usando a CPU naquele instante)
2. Pronto (Executável, temporariamente parado para deixar outro processo ser executado)
3. Bloqueado (Incapaz de ser executado até que algum evento externo aconteça).

![[Escalonamento.excalidraw]]

**Transições**:
 1. A transição 1 ocorre quando o sistema operacional descobre que o processo não pode continuar agora, quando por exemplo, o processo lê de algum arquivo especial e não há entrada agora, ele é bloqueado
 
 >*As transições 2 e 3 são causadas pelo [[Escalonamento]] de processos, uma parte do sistema operacional

2.  A transição 2 ocorre quando o **escalonador** decide que o processo em andamento foi executado por tempo suficiente, e é o momento de deixar outro processo utilizar a CPU.
3. A transição 3 é o outro lado da moeda da transição 2, o processo que antes aguardava a vez de usar a CPU agora está em execução, selecionado pelo escalonador.
4. A transição 4 checa se o evento que o processo estava esperando na transição 1 aconteceu, isto é, no exemplo dado, se uma entrada está disponível, neste caso, se não houver processos pendentes ele pode passar direto para a transição 3, ou, por um curto período aguardar em estado **pronto**.


#### Implementação de Processos

Para implementar o modelo de processos, o sistema operacional mantém um arranjo de estruturas chamada **tabela de processos**, com uma entrada para cada processo, as entradas contém informações importantes sobre o estado do processo, incluindo seu [[Contador de Programa]], [[Ponteiro de Pilha]], alocação de memória e estado dos arquivos abertos e tudo mais que deva ser salvo para quando o processo chavear de *em execução* para *pronto*, e posteriormente conseguir retomar como se nada tivesse acontecido.

Existe um local na memória, geralmente fixo, chamada de **vetor de interrupção**, que contém o endereço da rotina de serviço de interrupção. Supondo que um processo foi interrompido por uma interrupção de disco, [[Contador de Programa]], a palavra de estado e um ou mais registradores são salvos na pilha (atual) pelo hardware, o computador então desvia a execução pro endereço especificado no **vetor de interrupção**, e depois retoma.