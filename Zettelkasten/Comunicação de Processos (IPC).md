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

