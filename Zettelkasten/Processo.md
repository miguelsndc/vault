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