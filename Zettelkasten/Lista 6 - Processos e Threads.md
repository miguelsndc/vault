---
tags: arqcomp
---

$1)$ Um processo possui um espaço de memória dedicado a ele, onde pode ler e escrever, possui dados sobre variáveis globais arquivos abertos, sinais e tratadores de sinais, possui informações de contabilidade/gerenciamento, prioridade e escalonamento, possui uma ou mais threads de execução com pilha, contadores de programa, pilha e registradores.

$2)$ Contexto de hardware guarda informações correspondentes aos registradores do processo, ponteiros para pilha e estado. A troca de contexto de hardware salva as informações do contexto de hardware do processo $A$, carrega as informações do processo $B$ e executa o processo $B$, ao terminar, carrega as informações do processo $B$ e o retoma.

$3)$ Contexto de software armazena os limites e características dos recursos que podem ser alocados pelo processo, composto por três grupos principais:
- Identificação: ID do processo, ID do processo criador (PID)
- Quotas: Limite de arquivos abertos simultaneamente, limite de memória ocupada, operações de IO pendentes, número de threads.
- Privilégios: definem quais ações o processo pode fazer em relação a si, aos outros processos e ao sistema operacional

$4)$ Os processos possuem um espaço lógico de memória que pode ler e escrever, endereçado de $0$ a algum máximo. E cabe ao sistema operacional mapear esses endereços lógicos para endereços físicos na memória, e o faz através da MMU (Memory Management Unit). Essa abstração é útil para evitar que processos interfiram na memória reservada para outros processos, e para dar ao sistema operacional liberdade para mover processos de lugar na memória.

$5)$ Os processos são implementados através de tabelas de processos, onde cada entrada é chamada de "bloco de controle", e contém todas as informações necessárias do processo, contexto de hardware, software e espaço de endereçamento.

$5)$ Processos podem estar:
- Em execução (Executando normalmente)
- Prontos (executáveis, aguardando vez na CPU)
- Bloqueados (Aguardando alguma saída de outro processo ou IO)

$7)$ Processos que interagem com o usuário e servem a ele são os processos em foreground, processos que não interagem diretamente com humanos mas tem uma função específica são os processos em background, chamados **daemons**, por exemplo, um daemon de e-mails que de tempos em tempos checa se há algum e-mail novo para notificar o usuário de sua chegada.