---
tags: arqcomp
---
Uma técnica simples para criar [[Espaço de Endereçamento]] em memória, é utilizar de dois registradores para cada CPU, chamados de **registrador base e limite**, quando esses registradores são usados, os programas são carregados de forma contígua sempre que possível, e sem realocação durante o carregamento, e o registrador base é carregado com o início do bloco de memória reservado ao processo, e o registrador limite é carregado com o tamanho do programa, daí já viu. Cada instrução de memória é offsetada pelo valor no registrador base e checada para ver se ultrapassa o endereço limite.
Uma desvantagem é a necessidade de realizar uma adição e uma comparação a cada referência de memória, o que gera um tempo extra de carry, e torna o processo mais lento.
