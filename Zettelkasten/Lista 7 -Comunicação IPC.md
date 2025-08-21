
$1)$ Por conta do chaveamento de contexto, se um processo lê uma varíavel e, antes que possa a atualizar, a CPU decide escalonar outro processo, que também lê a variável, só que dessa vez, consegue atualizá-la, quando o controle voltar pro primeiro processo, ele vai atualizar para o valor que já está na variável, ou seja, uma atualização é perdida.


$2)$ Condições de disputa são situações desagradáveis onde processos manipulam áreas de memória compartilhada de tal forma que causam inconsistência nos dados ou outros problemas como starvation ou deadlock, essas áreas de memória ou arquivos compartilhados são chamados de seções críticas, tendo em vista que há ocasiões em que desastres acontecem por conta de sua manipulação. A solução para o problema chama-se exclusão mútua, onde dois processos jamais podem entrar em suas seções críticas simultaneamente, existem quatro condições a serem atendidas:
- dois processos não entram em SC ao mesmo tempo
- Nenhuma suposição de número de cpus ou velocidade pode ser feita
- Um processo fora de seção crítica pode bloquear outro processo
- Nenhum processo deve esperar eternamente para entrar em SC

$3)$ Interrupções podem ser desabilitadas somente para uma CPU, um processo executando em outra CPU pode continuar acessando a SC ao mesmo tempo do atual, e bloquear todas as outras CPU's é impensável. Além de que dar a um processo o poder de desabilitar interrupções é crítico, e se ele nunca reabilitar ? Não é crível dar a processos poder que somente o SO em modo núcleo deve possuir.


$4)$ Busy wait tem o problema da inversão de prioridades, quando um processo de prioridade baixa entra em seção crítica e um processo de prioridade máxima executa em espera ocupada, o processo é executado de tal forma que o escalonamento nunca vai escalonar o processo de menor prioridade, então ele nunca tem a chance de deixar a seção crítica, então o processo de menor prioridade fica bloqueado e o de maior fica em loop infinito.

$5)$ Starvation acontece quando um processo espera eternamente para entrar em sua região crítica.
Deadlock's acontecem quando dois ou mais processos ficam bloqueados eternamente por conta de alguma race condition.

$6)$ Semáforos são mecanismos que permitem implementar, ao mesmo tempo:
- Exclusão mútua
- Sincronização
- Algoritmos de escalonamento

Semáforos são variáveis inteiras não negativas que podem se manipuladas por duas instruções, **atômicas e indivisíveis**, chamadas de *down* e *up*:

- Down dre


$8)$ O esquema de alternância obrigatória assume que os processos estritamente se alternam em suas regiões críticas, se ambos não estão em RC, um aguarda o outro terminar suas tarefas não críticas para poder entrar em região crítica, o que fere o terceiro princípio.


