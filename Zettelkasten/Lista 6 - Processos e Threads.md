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

$1.2)$ Uma aplicação pode criar a ilusão de concorrência alternando o tempo de CPU entre processos, dando a cada um uma parcela justa de tempo de CPU para que todos os processos consigam progredir.

$2.2)$ Chaveamento de contexto inerente à atividade de alternar o tempo de CPU é um problema grave de desempenho, dado que processos são entidades pesadas e complexas. 

$3.2)$ Threads são as unidades de execução de um processo, um processo pode ter várias threads associadas a ele, as threads compartilham os dados do processo, as variáveis globais, o espaço de endereçamento e arquivos abertos, as vantagens das threads estão em que uma thread é ordens de grandeza mais rápidas de serem criadas, e podem ser orquestradas de tal forma que chamadas de sistema bloqueantes podem ser executadas por uma thread, esta thread ser bloqueada e as outras continuarem executando. Ao invés de ter um processo inteiro bloqueado, temos apenas uma thread, que é mais rápida de se reerguer, e pode haver outras threads realizando trabalho para aquele processo concorrentemente.


$4)$
- A
- B
- B
- A
  B
- A
- A/B

$5)$ A vantagem mais clara é que as threads podem compartilhar a memória para cooperar entre si e dividir o trabalho. A desvantagem também mais evidente é que não existe proteção entre threads, porque é impossível, já que é inerente às threads o compartilhamento do espaço de endereçamento, e também porque as threads tem o intuito de cooperar e não lutar entre si, por conta disso, threads podem alterar os valores da pilha de outras threads, causar race conditions, entre outros.


$6)$ Pacotes de threads em modo usuário são orquestrados por software por um sistema de tempo de execução, que escalona as threads entre si. O sistema enxerga cada thread como um processo monothread separado, o que traz a desvantagem de que, se o processo ceder tempo de CPU para outro processo, todas as suas threads são bloqueadas. Também, caso uma thread faça uma chamada de sistema bloqueante, todas as outras threads também são bloqueadas, o que é inaceitável, já que perde o propósito do multithreading. No modo núcleo, o núcleo enxerga todas as threads, e possui uma tabela para identificar cada thread, seu contexto de hardware, etc. E as ações são executadas como chamadas de n
