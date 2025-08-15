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

#### Threads de Usuário

Threads de usuário são implementadas pela biblioteca de threads no modo usuário. O sistema operacional as enxerga como um único processo com uma única thread de núcleo. Entre as vantagens, temos que o chaveamento entre threads de usuário é extremamente rápido, pois não envolve o kernel: quando uma thread executa algo que pode bloqueá-la localmente, é possível que haja um escalonador de threads local que armazena as informações das threads — contador de programa, pilha, registradores etc. — em uma tabela de threads e as orquestra. Como o escalonamento é local e nenhuma chamada ao kernel é feita, o chaveamento de threads é ordens de magnitude mais rápido que o chaveamento de processos.

Entre as desvantagens, temos os casos de _page faults_ e outras chamadas de sistema bloqueantes: uma vez que uma thread faça uma chamada bloqueante, todas as outras ficam bloqueadas aguardando, o que é absolutamente inaceitável e tira todo o propósito de se usar threads, que é permitir que apenas a thread bloqueada pare, enquanto as outras continuam executando. Alternativas para esse comportamento exigem mudanças internas na biblioteca ou no sistema operacional, o que normalmente não é atrativo.

Outra desvantagem é que, uma vez que uma thread de usuário comece a ser executada, nenhuma outra thread do mesmo processo será executada até que a primeira libere voluntariamente a CPU. Dentro de um único processo não há interrupções de relógio geridas pelo kernel para threads de usuário, tornando impossível implementar escalonamento circular de forma automática. Existe a possibilidade de forçar o sistema de tempo de execução (coleção de rotinas que gerencia as threads) a solicitar sinais de temporizador para retomar o controle, mas isso gera sobrecarga e aumenta a complexidade.

O argumento mais devastador é que, em aplicações que mais se beneficiam de threads — por exemplo, servidores web, que estão constantemente realizando chamadas bloqueantes —, o uso de threads de usuário elimina justamente o motivo para utilizá-las, tornando o conceito ineficaz nesses casos.

#### Threads de Núcleo

Ao invés de cada processo possuir uma tabela de threads e um sistema de tempo de execução, o núcleo agora tem uma tabela que controla todas as threads do sistema. A criação e destruição de threads é feita a partir de chamadas de núcleo, que atualizam essa tabela. A tabela de threads armazena todas as informações relativas às threads — registradores, estado, etc. — que, no caso das threads de usuário, ficariam no espaço do usuário. O núcleo mantém, paralelamente, a tabela de processos tradicional para controle dos processos.

Todas as chamadas que poderiam bloquear uma thread são agora feitas como chamadas de sistema, a um custo consideravelmente maior do que uma chamada à uma rotina do sistema de tempo de execução. Quando uma thread é bloqueada, o sistema tem a opção de executar outra thread do mesmo processo (se houver) ou de outro processo. Enquanto isso, no modelo de threads de usuário, o sistema de tempo de execução escalona as threads do seu processo até que o núcleo retire a CPU dele ou não haja mais threads prontas.

Tendo em vista o custo maior de criação e destruição de threads, quando uma thread se encerra, o sistema pode marcá-la como não executável e reaproveitá-la depois para outra execução — ou seja, o sistema recicla threads, poupando parte do trabalho de criação, apenas modificando o necessário das estruturas internas da thread para abrigar a nova. Essa reciclagem também é possível no modelo de threads de usuário, mas como o custo de gerenciamento nesse caso é muito menor, há menos incentivo para fazê-lo.

Entre as vantagens do modelo de threads de núcleo, está a capacidade de lidar melhor com _page faults_ e chamadas bloqueantes: se uma thread provocar uma falta de página, o núcleo pode facilmente verificar se há outras threads executáveis no mesmo processo e executá-las enquanto aguarda o carregamento da página do disco.

Ainda assim, há problemas não resolvidos. Por exemplo, quando um processo com múltiplas threads é bifurcado (_fork_), o novo processo deve herdar todos os threads ou apenas um? A escolha depende do que será feito a seguir: se o processo for chamar _exec_ para iniciar um novo programa, provavelmente apenas um thread é a melhor escolha; se for continuar a execução, reproduzir todos os threads pode ser mais adequado.

Outra questão são os sinais. No modelo clássico, sinais são enviados para processos, não para threads. Surge, então, a dúvida: quando um sinal chega, qual thread deve tratá-lo? Uma solução seria permitir que threads registrassem interesse em sinais específicos, mas isso levanta outro problema: e se várias threads registrarem interesse pelo mesmo sinal?

#### Implementações Híbridas

Várias formas de contornar as desvantagens claras de threads de usuário/núcleo foram criadas ao longo do tempo, uma delas é uma abordagem que usa as threads de núcleo juntamente com threads de usuário, esta sendo multiplexada em algumas ou todas as de núcleo. Neste caso, o núcleo está consciente **somente** das threads de núcleo e as escalona.