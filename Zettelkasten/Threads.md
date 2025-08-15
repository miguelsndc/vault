---
tags: arqcomp
---

Threads são unidades de execução dentro de um processo que compartilham o mesmo [[espaço de endereçamento]] do processo criador. A criação de threads é geralmente muito mais rápida do que a criação de processos completos. Threads permitem comunicação eficiente e compartilhamento de memória entre si, e podem continuar executando mesmo quando outras threads estão bloqueadas em chamadas de sistema, o que pode trazer ganhos de desempenho significativos em aplicações adequadas.

Pode-se enxergar processos como a união de dois conceitos independentes: **agrupamento de recursos e execução**, um processo agrupa os recursos do seu programa, código, espaço de memória, disco, etc. Um processo possui o conceito de thread, que são linhas de execução, que possuem [[Contador de Programa]], registrador, pilha.

O que as threads adicionam no modelo de processo é permitir que hajam múltiplas instâncias de execução no mesmo processo, com um grau significativo de independência. Não há proteção entre threads, uma thread pode apagar/ler/escrever os dados da pilha de outra thread, isto acontece porque:
1. É impossível
2. Desnecessário
É impossível dado vista de que as threads compartilham o mesmo espaço de endereçamento, caso cada thread fosse ter memória própria, arquivos, etc, ela seria um processo separado, não uma thread. Outro motivo é que as threads pertencem ao mesmo processo que foi criado pelo mesmo usuário, para cooperar entre si, ao invés de processos, que podem ser hostis uns aos outros. O que se quer alcançar com uma thread é que se haja múltiplas instâncias de execução **cooperando**, e não **lutando**.

É importante notar que cada thread tem sua pilha, dado que é uma linha de execução independente, uma thread pode executar uma rotina Y enquanto outra thread executa uma rotina X, então, é necessário que cada thread possua sua história de execução. 

Uma thread, assim como processo, pode estar pronta, pode estar bloqueada, pode dar a vez para outra thread ocupar tempo de CPU, pode executar normalmente, pode estar bloqueada por chamadas de sistema, aguardando entrada, etc. Tudo relacionado à execução pode ser vista como feita por uma thread.

| **Itens por processo**        | **Itens por Thread** |
| ----------------------------- | -------------------- |
| Espaço de endereçamento       | Contador de programa |
| Variáveis globais             | Registradores        |
| Arquivos abertos              | Pilha                |
| Processos filhos              | Estado               |
| Alarmes pendentes             |                      |
| Sinais e tratadores de sinais |                      |
| informação de contabilidade   |                      |
Quando um processo é criado, ele possui uma thread única, essa thread pode criar outras com ajuda de rotinas de criação

#### Modelo POSIX

Aqui estão listadas alguma funções do modelo POSIX para threads, o standard `pthreads`:

- `pthread_create` Cria uma nova thread
- `pthread_exit` Conclui a chamada de thread (mata a thread)
- `pthread_join` Espera pela saída de uma determinada thread (bloqueia a thread que fez a chamada)
- `pthread_yield` libera a CPU para que outra thread seja executada


