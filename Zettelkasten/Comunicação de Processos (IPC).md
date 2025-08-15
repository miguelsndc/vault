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

