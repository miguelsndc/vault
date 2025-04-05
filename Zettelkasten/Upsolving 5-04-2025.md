---
tags: maratona
---

### Feitas

B - **Trivial** **Problem**
>[!faq] Número achar os números n e a quantidade de numeros q tem exatamente **m** trailing zeroes no final de n!.

Notando que $2\cdot 5= 10$, e sempre q se multiplica por 10 adiciona-se um zero na direita, basta achar quantos pares $2\cdot5$ existem em $n!$. Como existem bem mais 2's do que 5's, o problema se reduz a encontrar o número de 5's em n!. Mantendo um contador da quantidade de 5's o problema pode ser resolvido em $n\log_{5}n$. Note que caso $x$ tenha exatamente os $m$ zeros que a gente precisa, o próximo multiplo de 5 depois de $x$ já tem um zero a mais, ou seja, a quantidade sempre é $5$ e os números sempre são $x, x+1,x+2,x+3$ e $x+4$.

D - **pSort**
>[!faq] Tendo uma permutação de números de 1 a $n$ e um array dizendo a distância $d$ pra cada $i$, na qual um elemento na posição $i$ pode dar swap com outro na posição $i + d, i -d$, é possível fazer $1$ a $n$ ser igual a outra permutação dada no input ? O número de movimentos é ilimitado

A observação da questão se resume a perceber que caso um $p_{i}$ alcance outro elemento, isso forma uma aresta não direcionada, que diz basicamente *"da pra trocar esses dois"*, e isso forma um grafo no qual um caminho de um vértice $u$ pra um vértice $v$ significa que $u$ consegue ter $v$ como valor.

Então basta construir esse grafo e checar pra cada $i$ se existe um caminho pra posição desejada, como a constraint é $n \le 100$, é possível fazer com dfs, mas caso fosse maior dava pra fazer com **dsu**, checando se estão no mesmo componente.

F - **Bear Poker**

Minha solução foi meio bucha, dava pra ter feito só dividindo cada um por 2 ou 3 e depois ver se todos são iguais. Mas, descrevendo a solução, seria deixar $x=mmc(v[i],v[i + 1]) / v[i]$ e $y=mmc(v[i], v[i+1])/v[i + 1]$. se a fatoração de $x$ e $y$ fosse composta **somente** por 2's e 3's, é possível realizar a operação. Eu deveria ter pensado na **operação inversa** ao que o problema pede, teria sido uma resolução mais smooth.

J - **Shell Game**

é basicamente criar um vetor e dar swap, não tem muito o que fazer, **lembrar de prestar atenção caso o input seja em algum arquivo, perdi 20 minutos de penalidade por isso.** 

L - **Brick Wall**

é sempre ótimo colocar bloquinhos horizontais de $1\times2$, dito que é o menor bloquinho possível, sendo assim a solução é $\frac{mn}{2}$ caso $m$ seja par, e $(m)$