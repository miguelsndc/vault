---
tags: arqcomp
---

A necessidade de haver comunicação entre [[Processo]]s surge naturalmente, em casos como um *pipeline*, onde a saída de um processo é passada como entrada para outro processo, essa "passagem",  de informações precisa acontecer de alguma forma. Também em casos onde um processo escreve em algum buffer e outro processo lê e usa esses dados para algum fim. Esses processos podem compartilhar dados a partir de alguma estrutura de núcleo na memória principal, ou algum arquivo compartilhado, independente da natureza dessa informação, os problemas são os mesmos.

#### Condições de Corrida

Considere uma fila de impressão $S$ e dos processos $A$ e $B$, a fila possui posições $0,1,2,\cdots$ e duas variáveis, $in$ para apontar a próxima posição livre da fila, e $out$ para indicar o próximo arquivo a ser impresso, essas variáveis podem muito bem ser mantidas em arquivos de duas palavras disponíveis para todos os processos. Digamos que o processo $A$ leu $in$ e armazenou o valor em alguma variável $X$, escreveu o arquivo e atualizou $X = X + 1$ , e digamos que, logo em seguida, a CPU decide que $A$ ocupou a CPU por tempo o suficiente, e passa a executar $B$, que faz o mesmo. A fila de impressão segue normalmente, pois está consistente, o arquivo de $B$ é impresso enquanto que $A$ nunca terá seu arquivo, e esperará por anos por um retorno que nunca acontecerá. Condições como esta onde um arquivo atropela outro e o deixa estagnado, são chamadas de **condições de corrida**, condições como essa, onde o resultado depende de quem executou precisamente e quando.