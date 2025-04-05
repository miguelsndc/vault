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

Se pedisse o mínimo, um **bfs** pra achar o menor caminho seria possível, e caso fosse limitado $\le k$, bastaria achar os menores caminhos e ver se a soma dos menores possíveis é $\le k$.

F - **Bear Poker**

Minha solução foi meio bucha, dava pra ter feito só dividindo cada um por 2 ou 3 e depois ver se todos são iguais. Mas, descrevendo a solução, seria deixar $x=mmc(v[i],v[i + 1]) / v[i]$ e $y=mmc(v[i], v[i+1])/v[i + 1]$. se a fatoração de $x$ e $y$ fosse composta **somente** por 2's e 3's, é possível realizar a operação. Eu deveria ter pensado na **operação inversa** ao que o problema pede, teria sido uma resolução mais smooth.

J - **Shell Game**

é basicamente criar um vetor e dar swap, não tem muito o que fazer, **lembrar de prestar atenção caso o input seja em algum arquivo, perdi 20 minutos de penalidade por isso.** 

L - **Brick Wall**

é sempre ótimo colocar bloquinhos horizontais de $1\times2$, dito que é o menor bloquinho possível, sendo assim a solução é $\frac{mn}{2}$ caso $m$ seja par, e $\frac{(m -1)n}{2}$ caso $m$ seja ímpar, porque daí é só colocar um blocão vertical, e a diferença diminui $1$ ponto, que é o mínimo, porque se não fosse, teríamos q colocar mais um bloco vertical, o que diminuiria o score, ou o número de blocos horizontais não seria máximo, o que é uma contradição.

## Upsolving

- [ ] A - Kill the Monster
- [ ] C - Mishkin Energizer
- [ ] E - The number of products
- [ ] G - Red Green Towers
- [ ] H - Yet Another Promotion
- [ ] I - Vasya and Wrestling
- [ ] K - After Training


K - After Training

Como ele pede pra sortar pela contagem, depois pela distancia pro meio, e depois pelo número, por algum motivo que desconheço, colocar isso num array e numa priority queue pra sortar lexicograficamente não funciona, **lembrar de não ficar preso o tempo inteiro na mesma ideia, é frustrante e ineficiente.** Um padrão é gerado, no qual se inicia pelo meio, se divide em dois ponteiros, um q diminui e outro q aumenta, o que diminui tem prioridade pelo enunciado. Sempre que se chega no último ponteiro, o padrão se repete até q n seja esgotado.

Então achando o padrão e só jogando num array até o tamanho desse array ser $\ge n$ deve ser o suficiente não tem como o array ser grande o suficiente pra dar mle, pq a gente quebra quando chega em $n$.

**não ignorar ideias, considere tudo**

**Edge case**: caso $m$ seja par, então o  meio é $2$