---
tags:
---

O espaço de endereçamento de um [[Processo]] é o espaço da memória que pode ser utilizado por um processo para ler e escrever, indexado de 0 até algum máximo, o endereçamento é lógico, por exemplo, o processo pode enxergar seu espaço como de `0x0000000` até `0xFFFFFFF`, e cabe ao sistema operacional mapear esses endereços para endereços físicos na memória.

A vantagem dessa abordagem é que transfere a responsabilidade de gerenciar os endereços ao sistema operacional, garantido que processos não leiam/escrevam em espaços de outros processos, e também dão ao sistema operacional a capacidade de mover os processos de lugar na memória, caso eles requisitem mais memória ou simplesmente seja vantajoso os mover de posição. 