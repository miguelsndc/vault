---
tags: maratona
---

### B - Powerful String

A questão te pede basicamente pra achar uma inversão no array, onde i < j e freq[i] > freq[j], então para fazê-lo, existem algumas opções, a melhor solucao q eu vi foi a de palao, pra cada caracter guarda as posiçoes q ele aparece, pra fazer emquery em [l, r] basta achar lowerbound de l e prev(upper bound de r), claro tratando os casos onde eles nao existam, a frequencia, pra cada caracter pega o mais a esquerda e o mais a direita no range, dps em O(26^2) checa todos os pares e encontra a inversão.

foi relativamente proximo a solução q eu pensei no contest q n foi pra frente.