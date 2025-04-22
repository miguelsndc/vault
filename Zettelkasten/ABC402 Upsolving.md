---
tags: maratona
---

> A and B went smoothlyj

### C - Dislike Foods -  [link](https://atcoder.jp/contests/abc402/tasks/abc402_c)

Takahashi era frango e nao gostava de um monte de ingredientes,cada comida tem um conjunto distinto de ingredientes, a cada dia que passa takahashi desaviada com um ingrediente, tu tem que printar, pra cada dia, quantas comidas ele pode comer se ele desaviadar com o ingrediente $b[i]$.

Tentei pensar num brute force mas não tem como com as constraints, (tudo $\le 3 \cdot10^{5}$), seria pra cada dia passar por cada comida e deletar o ingrediente, o que é $O(N M \Sigma k_{i} )$, que basicamente cubico.

A questão é que uma comida só se torna disponivel quando o ultimo ingrediente que ela tem, na ordem dos $b[i]$ é consumido, então pra cada comida eu só tenho que saber qual a ultima posição em b que é um ingrediente dessa comida, então é só somar quando chego lá, pode se usar um vetor e ir fazendo uma soma acumulada.

### D - 