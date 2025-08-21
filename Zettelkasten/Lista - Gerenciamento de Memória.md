---
tags: arqcomp
---

$1)$ Três funções do gerenciamento de memória são:
1. Manter o máximo de processos em memória possível, pois buscas na memória secundária são lentas e prejudicam o desempenho do sistema.
2. Manter o controle de quais partes estão ocupadas/livres na memória.
3. Alocar/liberar a memória dos processos.

$2)$ Como o programa do usuário ocupa 768MB e o programa apenas $512$KB $=$ 0.512MB, temos uma subutilização de praticamente 100%, sendo memória utilizada: $\frac{0.512}{768}=0.00066$, e $100\% -0.0006 = 99.99933.. \approx 100\%$. 

$3)$ O programa C proporciona maior taxa de utilização por ser maior e caber na memória, o programa $B$ não cabe no espaço disponível, e o $A$ ocupa menos memória, causando maior subutilização.

$3)$ Fragmentação *interna* refere-se a taxa de subutilização do espaço de memória alocado a um processo. O espaço desperdiçado pelo processo.

Fragmentação externa acontece quando a memória principal livre está dividida em vários pedaços pequenos inúteis, que não comportam nenhum processo que será alocado, podemos ter blocos de 2, 3, 1, 2 e 2MB livres, totalizando 10MB livres e um processo que necessita de 10MB não poderá ser alocado, mesmo tendo esse espaço **fragmentado** na memória.

$3)$

$a)$ O módulo principal deve ser mantido da memória, uma região do tamanho do maior módulo deve ser reservada, então os módulos os independentes sendo transferidos do disco pra memória e vice-versa, conforme necessário, sobrescrevendo a memória do módulo presente.

$b)$ Quando o módulo presente não ocupa toda a memória ocorre fragmentação interna.

$c)$ (150 + 200 + 300) / 3 $\approx$ 216, com modulo principal + SO temos 216 + 128 = (408) / 512 = $79\%$ de utilização da memória principal.

$d)$ não, pois o módulo maior de 350KB nunca seria executado.

### Parte II 

$1)$ A técnica de swapping serve para "manter" mais processos ativos do que a memória principal permite, movendo-os entre memória e disco com base em alguma política.

$2)$ Existe um registrador de *relocação* que recebe o endereço inicial da posição de memória que o processo irá ocupar, então toda referência posterior é somada ao valor desse registrador a fim de obter o endereço físico, com isso o programa pode ser carregado em qualquer posição de memória no *swap-in*.

$3)$ Quando há pouca memória disponível, o sistema pode ficar inteiro dedicado a fazer swapping, dado o custo elevando da operação (busca no disco), o desempenho é seriamente comprometido.

$4)$ É uma estratégia para lidar com bloatware, programas que excedem o tamanho da memória principal disponível, a técnica se resume à dividir o programa em blocos de tamanho fixo chamados de páginas, e esses páginas podem existir na memória principal como **quadros de página** ou no disco. Quando o processo referencia um endereço em uma página que está no disco, a MMU desvia pro sistema operacional e ele busca no disco, atualiza o quadro de páginas e reexecuta a instrução que falhou.

$5)$ 
- Minimiza a fragmentação, já que os programas podem ser alocados em espaços não contíguos.
- Programas deixam de estar limitados ao tamanho da memória física disponível.
- Permite maior compartilhamento de memória já que apenas parte de cada processo fica presente na memória e melhor utilização da CPU.

$6)$ Espaço de endereçamento virtual se refere aos endereços que o processo pode referenciar e que serão futuramente traduzidos em endereços físicos pela MMU.  O espaço de endereçamento real são os endereços físicos.

$7)$ A **tabela de páginas** é utilizada.

$8)$ Pode ser implementada com **paginação**, onde os blocos de memória são divididos em páginas de tamanho fixo, **segmentação**, de tamanho variável, ou ambos. 

$9)$ Paginação os blocos tem tamanho fixo, e em segmentação, variável.

$10)$ O endereço virtual é composto por:
- Número de página virtual (NPV): índice para a tabela de páginas virtuais.
- Deslocamento de página, que indica o deslocamento referente ao início do programa.
O endereço física é obtido combinando o endereço do frame junto com o deslocamento.

$11)$ Quando a página não se encontra presente na memória ocorre um **page fault** (falta de página), a MMU detecta que a página não se encontra nos quadros de página, gera uma interrupção e o sistema operacional se encarrega de executar alguma política de troca de páginas, onde ele escolhe uma página do quadro em função dessa política e joga pro disco, e traz de volta a página que precisa ser referenciada, diz o número dessa página e reexecuta a instrução que falhou.

$12)$ Paginação apresenta fragmentação interna, a 