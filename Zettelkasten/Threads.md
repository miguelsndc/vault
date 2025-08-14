---
tags: arqcomp
---

Threads são unidades de execução dentro de um processo que compartilham o mesmo [[espaço de endereçamento]] do processo criador. A criação de threads é geralmente muito mais rápida do que a criação de processos completos. Threads permitem comunicação eficiente e compartilhamento de memória entre si, e podem continuar executando mesmo quando outras threads estão bloqueadas em chamadas de sistema, o que pode trazer ganhos de desempenho significativos em aplicações adequadas.

Pode-se enxergar processos como a união de dois conceitos independentes: **agrupamento de recursos e execução**, um processo agrupa os recursos do seu programa, código, espaço de memória, disco, etc. Um processo possui o conceito de thread, que são linhas de execução, que possuem [[Contador de Programa]], registrador, pilha.

O que as threads adicionam no modelo de processo é permitir que hajam múltiplas instâncias de execução no mesmo processo, com um grau significativo de independência