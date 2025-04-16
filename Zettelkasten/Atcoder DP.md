---
tags: maratona
---

Soluçoes e comentarios e piadas e coisas sobre o contest educacional de dp do atcoder. A forma mais simples de dp é fazer um backtracking memoizado, evitando passar por certos estados, da pra inferir quais estados ele vai passar e meio que chutar uma complexidade, da pra resolver uma parte razoavel dos problems assim, mas caso não, soluções iterativas e um dp recursivo mais esperto seja possivel

### C - Vacation

O problema te da um conjunto de triplas onde vc deve escolher exatamente uma dos elementos de cada tripla e nao pode haver repetição entre escolhas consecutivas

A DP se resume a o indice que vc esta *i* e qual vc escolheu anteriormente, pra conseguir filtrar os que vc vai escolher agora, pra memoizar basta uma tabela com uma dimensao pro indice e outra pra prev.

Aprendi um negocio interessante, aparentemente quando voce coloca mais ou menos parametros que o necessario na função que calca a dp topdown, essa função pode tanto fazer menos chamadas que o necessario ou fazer calculos desnecessarios, tentar limitar os parametros da função à exatamente o que voce quer memoizar no estado garante que a arvore seja exatamente o que vc planejou de começo, por isso que certas soluções minhas não funcionavam de jeito nenhum, eu mantinha o resultado como parametro, e para o mesmo estado, (a, b), chamar com resutlados diferentes invoca uma branch adicional na arvore que pode ferrar com os resultados.


