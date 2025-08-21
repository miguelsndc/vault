---
tags: arqcomp
---
Embora hajam boas estratégias para gerenciamento de memória, como [[Swapping]] e os úteis [[Registradores Base e Limite]], ainda é preciso lidar com **bloatware**, *(programas que excedem o tamanho da memória disponível)*. Uma solução dada foi a **memória virtual**, que divide o [[Espaço de Endereçamento]] de um processo em blocos chamados **páginas**, que são **blocos contíguos de endereços** que são mapeados para a memória fisica mas nem todas as páginas precisam estar em memória ao mesmo tempo.
Caso o processo referencie um endereço que faz parte de uma página que esteja em memória física, o hardware rapidamente faz o mapeamento. Caso não, o sistema operacional é alertado para ir buscar a página que falta e reexecuta a instrução que falhou.


#### Paginação

Quando um processo referencia um endereço de memória, em uma instrução, esses endereços podem ser gerados por diversos métodos, por exemplo, [[Registradores Base e Limite]]. Esses endereços gerados são chamados de **endereços virtuais** e foram o **espaço de endereçamento virtual**, em computadores sem memória virtual, o endereço gerado é colocado diretamente no barramento de memória e faz com que a palavra física com o mesmo endereço seja escrita ou lida. Quando o computador possui esquema de **memória virtual**, os endereços antes passam pela ***MMU (Memory Management Unit)***, que vai mapear os endereços virtuais em endereços físicos.

O espaço de endereçamento virtual consiste em blocos de tamanho fixo chamados **páginas**, esses blocos que estão presentes na memória física são chamados de **quadros de páginas**, geralmente eles tem o mesmo tamanho.

As páginas são marcadas com um bit de presença que indica se elas estão na memória física ou não no mapa da MMU. Quando um endereço presente em uma página que não está em memória é referenciado, a MMU interrompe e desvia pro sistema operacional, isso se chama **page fault (falta de página)** e então uma rotina de:
- Escolher um quadro de página para mandar pro disco.
- Carrega do disco a página referenciada no quadro de página recém-liberado
		> Se o sistema operacional escolher a página 1 para ser substituída por exemplo, primeiro o SO marca a página 1 como não mapeada para evitar acessos nesse meio tempo, então marca o bit de presença na página que entrou.
- Reinicia a instrução que falhou.
