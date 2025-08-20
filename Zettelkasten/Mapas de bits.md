---
tags: arqcomp
---

Com um **mapa de bits** a memória é dividida em blocos de tamanho arbitrário, correspondendo a cada unidade de alocação (bloco), existe um bit no mapa de bits indicando se a memória está ocupada (1) ou vazia(0) (ou vice-versa).

O tamanho da unidade de alocação é fixo e é um aspecto importante do projeto, caso a unidade de alocação seja pequena, o mapa de bits será grande. Porém, mesmo num mapa de bits com uma unidade tão pequena quanto $4$ bytes, 32 bits de memória exigirão apenas um bit do mapa, então o mapa ocupa $\frac{1}{32}$ da memória. Se a unidade de alocação for definida como grande, o mapa de bits será menor, porém caso o tamanho dos processos não seja um múltiplo da unidade de alocação, uma grande parte de memória pode ser desperdiçada a custo de nada.

O principal problema do mapa de bits é que quando um programa de $k$ unidades de alocação precisa ser alocado na memória, temos o problema de encontrar uma janela de zeros de tamanho $k$ no mapa de bits 