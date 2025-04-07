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

- [x] A - Kill the Monster ✅ 2025-04-05
- [ ] C - Mishkin Energizer
- [x] E - The number of products ✅ 2025-04-05
- [ ] G - Red Green Towers
- [ ] H - Yet Another Promotion
- [x] I - Vasya and Wrestling ✅ 2025-04-05
- [x] K - After Training ✅ 2025-04-05


K - After Training

Como ele pede pra sortar pela contagem, depois pela distancia pro meio, e depois pelo número, por algum motivo que desconheço, colocar isso num array e numa priority queue pra sortar lexicograficamente não funciona, **lembrar de não ficar preso o tempo inteiro na mesma ideia, é frustrante e ineficiente.** Um padrão é gerado, no qual se inicia pelo meio, se divide em dois ponteiros, um q diminui e outro q aumenta, o que diminui tem prioridade pelo enunciado. Sempre que se chega no último ponteiro, o padrão se repete até q n seja esgotado.

Então achando o padrão e só jogando num array até o tamanho desse array ser $\ge n$ deve ser o suficiente não tem como o array ser grande o suficiente pra dar mle, pq a gente quebra quando chega em $n$.

**não ignorar ideias, considere tudo**

**Edge case**: caso $m$ seja impar, então o meio existe e é: $$\begin{align*}
1\;2\;\textbf{3}\;4\;5
\end{align*}$$
Neste caso deve-se priorizar o ponteiro da esquerda. caso m seja par:
$$\begin{align*}
1\;2\;\textbf{meio}\;3\;4
\end{align*}$$
Lembra um palíndromo. aí nesse caso deve-se priorizar o ponteiro da direita, porque caso se priorize o da esquerda, ele vai priorizar um elemento a esquerda q tem uma distancia maior que o da direita. nesse caso $m=2.5$ deve-se vir o $2$ depois o $3$, ambos com distancia $0.5$, caso se priorize o da esquerda vem-se o $2$ depois o $1$, e só depois o $3$, o que é errado.

I - **Vasya and Wrestling**

Não era necessário colocar nas strings pra ver qual era lexicograficamente menor, bastava salvar os números em algum lugar e ver qual era o maior um a um, também não era necessario salvar a soma pra cada um, era só colocar a soma numa variavel só, caso fosse zero teriamos um empate

e curiosamente não é necessario checar qual o maior em tamanho, basta ver qual o ultimo, mas checando também passa, o que é estranho.

E - **Number of Products**

> [!faq] calcule o número de pares de indices (l, r) com $l\le r$ tais que o produto de todos os elementos entre $a_{l}$ e $a_{r}$ é positivo/negativo

Primeiro vamos perceber que o problema se resume a calcular o número de subarrays com produto positivo **ou** negativo, não é necessário calcular ambos, o número de segmentos delimitados por (l, r) com l $\le$ r são $\frac{n(n + 1)}{2}$, se calcularmos o número de subarrays positivos e tirarmos de $\frac{n(n +1)}{2}$ teremos o número pros negativos.

A ideia é calcular, pra cada $i$, quantos subarrays com produto positivo terminam em $i$.

pra cada posição se a gente armazenar:
- **quantos elementos negativos apareceram: x**
- **quantos elementos tem um numero par de numeros negativos antes dele: y**
- **quantos elements tem um numero impar de numeros negativos antes dele: z**

se x for par então qualquer subarray terminando na posição atual e contendo um número par de numeros negativos deve começar numa posição onde a x era par também, ou seja, $y$, generalizando, caso queiramos um número par de números negativos precisamos contar quantas posições o subarray começa que tem a mesma paridade de números negativos que a atual, de tal forma, o resultado é par, que é o que queremos para contar os segmentos positivos.

#### O que é possível tirar desse problema

Conseguimos usar **prefixos/sufixos** para simplificar operações em intervalos utilizando uma espécie de **dp** implícita, onde lembramos algum valor pra cada posição do prefixo, então contamos, ***de quantas posições eu posso começar tal que a propriedade ainda é satisfeita e o subarray termina na posição que eu estou ?*** prefixos com mesma característica resultam em intervalos com a propriedade desejada.

- Identifique uma propriedade que pode ser calculada incrementalmente
- Rastreie frequência de diferentes estados dessa propriedade
- Para cada posição, use os contadores para determinar quantos subarrays válidos terminam ali

A - **Kill the Monster**

É uma questão que te dá um valor $k$ que tu pode gastar em upgrades, te dá a vida e ataque do teu personagem e a vida e ataque do monstro que tu tem que vencer. $w$ e $a$ são os valores que tu ganha de ataque e vida por moeda caso gaste 1 moeda.

Nesse caso basta a gente checar de 1 até k, todas as combinações lineares de upgrades, tipo $hc+i*a$ e $dc + (k - i) *w$, o que pode ser feito linearmente. para saber quem vence o duelo basta fazer uma continha: o número de ataques que o personagem precisa dar para matar o monstro precisa ser menor ou igual a quantidade de ataques que  monstro precisa dar para vencer, menor ou igual porque o personagem ataca primeiro, se eles derem o mesmo dano ele vence primeiro. então, o dano dado é $\lceil \frac{vida}{dano}\rceil$. basta checar se $\lceil \frac{hm}{dc}\rceil \le \lceil \frac{hc}{dm} \rceil$ . complexidade linear.

H - **Yet Another Promotion**

Note que é sempre ótimo comprar na promoção se $a m \le b(m+1)$, porque daí ganhamos uma batata de graça, então comprando essas batatas na promoção (ou não), o resto das batatas deve ser comprada a $min(a,b)$. 