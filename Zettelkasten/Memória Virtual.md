---
tags: arqcomp
---
Embora hajam boas estratégias para gerenciamento de memória, como [[Swapping]] e os úteis [[Registradores Base e Limite]], ainda é preciso lidar com **bloatware**, *(programas que excedem o tamanho da memória disponível)*. Uma solução dada foi a **memória virtual**, que divide o [[Espaço de Endereçamento]] de um processo em blocos chamados **páginas**, que são **blocos contíguos de endereços** que são mapeados para a memória fisica mas nem todas as páginas precisam estar em memória ao mesmo tempo.
Caso o processo referencie um endereço que faz parte de uma página que esteja em memória física, o hardware rapidamente faz o mapeamento. Caso não, o sistema operacional é alertado para ir buscar a página que falta e reexecuta a instrução que falhou.


#### Paginação