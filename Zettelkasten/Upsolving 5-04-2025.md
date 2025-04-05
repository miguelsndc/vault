---
tags: maratona
---

### Feitas

B - **Trivial** **Problem**
>[!faq] Número achar os números n e a quantidade de numeros q tem exatamente **m** trailing zeroes no final de n!.

Notando que $2\cdot 5= 10$, e sempre q se multiplica por 10 adiciona-se um zero na direita, basta achar quantos pares $2\cdot5$ existem em $n!$. Como existem bem mais 2's do que 5's, o problema se reduz a encontrar o número de 5's em n!. Mantendo um contador da quantidade de 5's o problema pode ser resolvido em $n\log_{5}n$. Note que caso $x$ tenha exatamente os $m$ zeros que a gente precisa, o próximo multiplo de 5 depois de $x$ já tem um zero a mais, ou seja, a quantidade sempre é $5$ e os números sempre são $x, x+1,x+2,x+3$ e $x+4$.

D - **pSort**
>[!faq] Tendo uma permutação de números de 1 a $n$ e um array dizendo a distância $d$ pra cada $i$, na qual um elemento na posição $i$ pode dar swap com outro na posição $i + d, i -d$, é possível fazer $1$ a $n$ ser igual a outra permutação dada no input ? 



