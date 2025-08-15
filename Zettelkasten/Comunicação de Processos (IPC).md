---
tags: arqcomp
---

A necessidade de haver comunicação entre [[Processo]]s surge naturalmente, em casos como um *pipeline*, onde a saída de um processo é passada como entrada para outro processo, essa "passagem",  de informações precisa acontecer de alguma forma. Também em casos onde um processo escreve em algum buffer e outro processo lê e usa esses dados para algum fim. Esses processos podem compartilhar dados a partir de alguma estrutura de núcleo na memória principal, ou algum arquivo compartilhado, independente da natureza dessa informação, os problemas são os mesmos.

#### Condições de Corrida

Considere uma fila de impressão $S$ e dos processos $A$ e $B$, a fila possui posições $0,1,2,\cdots$ e duas variáveis, $in$ para apontar a próxima posição livre da fila, e $out$ para indicar o próximo arquivo a ser impresso, essas variáveis podem muito bem ser mantidas em arquivos de duas palavras disponíveis para todos os processos. Digamos que o processo $A$ leu $in$ e armazenou o valor em alguma variável $X$, escreveu o arquivo e atualizou $X = X + 1$ , e digamos que, logo em seguida, a CPU decide que $A$ ocupou a CPU por tempo o suficiente, e passa a executar $B$, que faz o mesmo. A fila de impressão segue normalmente, pois está consistente, o arquivo de $B$ é impresso enquanto que $A$ nunca terá seu arquivo, e esperará por anos por um retorno que nunca acontecerá. Condições como esta onde o resultado depende de quem executou precisamente e quando, são chamadas de **condições de corrida**.


### Soluções para condições de corrida - exclusões mútuas

Se conseguíssemos garantir que, jamais dois processos acessassem uma informação compartilhada, sanaríamos o problema das condições de corrida. Isto é, um processo, de tempos em tempos, precisa acessar alguma informação compartilhada ou realizar alguma tarefa crítica que pode levar a corridas, essa região de memória ou arquivo acessada é chamada de **região crítica**. Se conseguirmos organizar as coisas de tal forma que apenas **um** processo está em uma região crítica de cada vez, resolvemos os problemas das corridas. Mas para ser correto e eficiente, não é tão simples assim, **quatro condições** precisam ser atendidas:

1. Dois processos jamais podem estar em suas regiões críticas simultaneamente
2. Nenhuma suposição pode ser feita a respeito de velocidade ou número de CPU's
3. Nenhum processo executando fora de sua região crítica pode bloquear outro processo
4. Nenhum processo deve ser obrigado a esperar eternamente para entrar em sua região crítica.


##### Desligamento de Interrupções

Uma das soluções é desligar os sinais de interrupção quando um processo está em sua região crítica, dessa forma, nenhum outro processo pode também executar, portanto não pode entrar em sua região crítica, esta abordagem é falha, dado que em um sistema multiprocessador, desabilitar interrupções em uma CPU somente não garante que processos executando em outras CPU's também acessem suas regiões críticas.
E também dar a processos o poder de desabilitar interrupções é desencorajado, e se o processo desabilitar e nunca mais reabilitar ? fim do sistema. Também desabilitar todas as CPU's quando um processo está em região crítica é tão ineficiente que chega a ser cômico.

##### Variáveis de Trava

E se houvesse uma varíavel que indicasse quando um processo está em região crítica ? Um processo primeiro checa se a variável de trava está livre $= 0$, e então a troca para $1$ e entra em região crítica. O problema de race conditions vai existir do mesmo jeito para essa variável, um processo lê a variável, vê que está $0$, e a CPU passa para outro processo, que também a lê a atualiza para $1$, e entra na região crítica, quando a CPU retomar o processo antigo, ele também a atualiza e entra em região crítica.

##### Alternância explícita

Esta abordagem utiliza de **espera ocupada**, que é uma estratégia onde o processo testa continuamente em loop contra uma variável para saber se é possível entrar em sua região crítica, o que é desencorajado, porque desperdiça tempo de CPU. 
j
Ainda assim, considerando a situação onde os dois processos não estão em suas regiões críticas, e a variável de turno indica um valor $x$, um processo deve aguardar o outro concluir sua região não crítica para poder entrar em sua região crítica novamente, o que fere o terceiro princípio de exclusão mútua, o que um processo fora da sua região crítica não pode bloquear um processo de entrar na sua. Alternância explícita, para funcionar corretamente exige que os processos alternem-se estritamente nas entradas pra suas RC.


#### A instrução TSL

A maioria dos processadores possui uma instrução atômica e indivísivel para setar uma varíavel de lock em um registrador, assim garantindo que nenhum processo entra em regiões críticas ao mesmo tempo, um processo fica em espera ocupada.


### Inversão de Prioridades

O grande problema de soluções que utilizam espera ocupada é exemplificada na situação a seguir: Imagine que existem dois processos $A$ e $B$, e $A$ é criado de tal forma que sua prioridade é tão alta que sempre que puder ser executado, ele será, indivisivelmente. Considere que $B$ entra em sua região crítica, e $A$ entra em espera ativa. Como $A$ está executando (esperando), ele nunca para de executar, e $B$ fica impossibilitado de deixar sua região crítica porque nunca tem a CPU para si, dada as prioridades.

#### Problema Produtor-Consumidor

Imagina o seguinte problema, temos um produtor, um consumidor, e um buffer, o produtor enche o buffer até que ele esteja cheio, então vai dormir, e o consumidor retira itens do buffer até que ele esteja vazio, e então vai dormir.
Os problemas de condições de corrida são os mesmos da fila de impressão, note que, se o consumidor ler uma variável `count` que indica quantos itens estão no buffer, e ela for 0, e logo em seguida o escalonador trocar para o produtor, ele vai ler, e atualizar o conteúdo pra 1, e então **acordar o consumidor, que não estava logicamente dormindo, então a instrução é perdida**, quando o escalonador retomar o consumidor, ele vai notar que o count que leu é $0$, e irá dormir, o produtor eventualmente vai encher o buffer, e ambos dormirão pra sempre, **deadlock**.

#### Semáforos

**Semáforos** são variáveis inteiras cujo valor é modificado apenas por **operações atômicas** (`wait`/`P` e `signal`/`V`), garantindo que não ocorram **condições de corrida**.

O valor de um semáforo indica **quantos recursos estão disponíveis** naquele instante, permitindo que múltiplas threads/produtores/consumidores acessem recursos compartilhados de forma sincronizada.

- **Semáforo contador**: pode assumir valores maiores que 1, controlando múltiplos recursos disponíveis.
- **Semáforo binário**: só assume 0 ou 1 e é funcionalmente similar a um _mutex_, mas não é exatamente o mesmo — um mutex é um mecanismo de **exclusão mútua** estrito, enquanto um semáforo binário pode ser usado também para **sincronização** entre threads que não compartilham exatamente a mesma seção crítica.

A exclusão mútua em si não é “implementada pelos contadores”, mas pelo uso de semáforo binário ou mutex para garantir que apenas uma thread entre na seção crítica por vez.

#### Mutex

Mutexes são simples variáveis 