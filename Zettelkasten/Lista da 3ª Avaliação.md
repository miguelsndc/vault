$\text{1 Questão}$:

$A = \{2,3,4,5,6,7,8\}$.
$xRy \iff x-y =3n$ para $n \in \mathbb{Z}$.
## *Verificando se é uma Relação de Equivalência*:
1. **Reflexividade**:
   Seja algum $a \in A$, o par $(a,a) \in R$ se $a-a = 3n$, o que se traduz em $0 = 3n$, e que é verdade para $n=0$, logo $R$ é reflexiva.
2. **Simetria**:
   Seja $(a,b)$ tal que $a-b = 3n$ e $a \gt b$. 
   Assume-se $a \ne b$ pois se $a = b$, pela reflexividade, tem-se que $(a,a) \in R$.
   Portanto o bar $(b,a)$ será tal que $b - a = -3n$, que é igual a $3(-n)$. Logo, para todo $n$ que satisfaz $(a,b)$, $-n$ satisfará $(b,a)$. Caso assumíssemos $a \lt b$, a demonstração é análoga, com a conclusão invertida.
3. **Transitividade**:
   Seja $(a,c) \in R$ e $(c,b) \in R$. Logo temos as seguintes expressões
$$\begin{align*}
a - c&= 3q, \;\; q \in \mathbb{Z}\\
c - b &= 3t, \;\;t \in \mathbb{Z}\\
\end{align*}$$
3. Somando temos:
$$\begin{align*}
(a-c)+(c-b)&= 3q + 3t\\
a-b &= 3(q+t)
\end{align*}$$
3. Portanto $(a,b) \in R$ e $R$ é transitiva, consequentemente, $R$ é uma relação de equivalência.
## Grafo
Listando os pares:
1. $(i,i), i = 2,3,4,5,6,7,8$ e $(2,5),(5,2),(3,6),(6,3),(4,7),(7,4),(5,8),(8,5), (8,2), (2,8)$.

![[grafo_1_.excalidraw]]
___
$\text{2 Questão}$

- *Reflexiva e simétrica, mas não transitiva*;

$S = \{1,2,3\}$
$R = \{(1,1), (2,2), (3,3), (1,2), (2,1), (2,3), (3,2)\}$
$R$ não é transitiva pois $(1,3) \notin R$.

- *Não reflexiva nem simétrica, mas transitiva*;

$S=\{1,2,3\}$
$R= \{(1,2),(2,3), (1,3)\}$
$R$ não é reflexiva pois $(1,1) \notin R$, e $R$ não é simétrica pois $(2,1) \notin R$.

- *Reflexiva mas não simétrica nem transitiva*

$S = \{1,2,3\}$
$R = \{(1,1), (2,2), (3,3), (1,2), (2,3)\}$.
$R$ não é simétrica pois $(2,1) \notin R$ e nem transitiva pois $(1,3) \notin R$.
___
$\text{3 Questão}$

$S = \{1,2,3,4,5\}$ e $R$ em $S$ com $R = \{(1,2), (2,1), (2,3), (3,4) (4,1), (5,1),(5,4)\}$.
- Fecho Reflexivo de $R$: $R \cup \{(1,1), (2,2), (3,3), (4,4), (5,5)\}$
- Fecho Simétrico de $R$: $R \cup$ $\{(3,2), (4,3), (1,4), (1,5),(4,5)\}$.
- Fecho Transitivo:
$1:2,1,3,4$

$2:1,3,2,4$

$3:4,1,2,3$

$4:1,2,3,4$

$5:1,4,2,3$
Logo o fecho transitivo é:$R \cup \{(1,1), (1,3),(1,4),(2,2),(2,4),(3,4), (3,2), (3,3), (4,2), (4,3), (4,4), (5,2),(5,3)\}$.
___
$\text{4 Questão}$

$S={A,B,C,D,E}$
Pelo grafo, a relação $R$ é $R= \{(A,A), (A,D), (A,B), (B,E), (B,C), (C,C), (C,B), (C,E), (D,E), (E,E), (E,A), (E,C), (E,D)\}$Com:
$A:A,B,C,D,E$ 

$B:C,E,A,B,D$

$C:B,C,E,A,D$

$D:E,A,B,C,D$

$E:A,D,E,B,C$
Temos que o fecho transitivo de $R$ é: $R \cup \{(A,C), (A,E), (B,A), (B,B), (B,D), (C,E),(C,A),(C,D),(D,A),(D,B),(D,C),(D,D),(E,B),(E,C)\}$
____
$\text{5 Questão}$

$R = \{(x,y) \mid x - y \in \mathbb{Z}\}$, relação em $\mathbb{R}$.
## *Provando que a relação é de equivalência:*
- **Reflexividade**:
  Seja $a \in R$, então $(a,a) \in R \iff a-a \in \mathbb{Z}$, como $a-a=0$ e $0 \in \mathbb{Z}$, $(a,a) \in R$.
  Portanto, $R$ é reflexiva.
- **Simetria**: 
  Seja $(a,b) \in R$, com $a-b = n, \;\; n \in \mathbb{Z}$. então $(b,a) \implies b-a = -n$, como $-n \in \mathbb{Z}$, $R$ é simétrica.
- **Transitividade**:
  Seja $(a,c) \in R$ tal que $a-c = x,\;\; x \in \mathbb{Z}$ e $(c,b) \in R$ tal que $c-b = y, \;\; y \in \mathbb{Z}$. Somando as duas expressões temos: $(a-c)+(c-b) = a-b = x + y$. Como $x+y \in \mathbb{Z}$, $(a,b) \in R$logo $R$ é transitiva.

$\text{b)}$ A Classe de equivalência de $1$ são todos os pares $(1,s)$ tal que $1 -s \in \mathbb{Z}$. Note que:
- $s = -1 \implies 1-(-1) = 2$
- $s = 1 \implies 1- 1 = 0$
- $s =0 \implies 1-0 = 1$
Contanto que $s \in \mathbb{Z}$, $1- (-s) = 1 + s \in \mathbb{Z}$, e $1-s \in \mathbb{Z}$
Portanto $[1]_{R} = \mathbb{Z}$.

$\text{c)}$ A Classe de equivalência de $\frac{1}{2}$ são todos os pares $(\frac{1}{2}, q)$, tal que $\frac{1}{2}-q \in \mathbb{Z}$, Note que:
- $q=0 \implies \frac{1}{2}-0 = \frac{1}{2}$, sabemos logo que $0 \notin [\frac{1}{2}]_{R}$.
- $q=\frac{3}{2} \implies \frac{1}{2} - \frac{3}{2} = \frac{-2}{2}=-1$.
- $q=\frac{-5}{2} \implies \frac{1}{2}-\left(- \frac{5}{2} \right)= \frac{6}{2}=3$
- $q = 2 \implies \frac{1}{2}- \frac{4}{2}= \frac{-3}{2}$ 
- $q = \frac{7}{8} \implies \frac{1}{2} -  \frac{7}{8} = \frac{-3}{8}$ 
Precisamos de um número ímpar com denominador $2$ para completar um inteiro:
Seja $\frac{m}{2} \in \mathbb{R}$, com $m \in \mathbb{Z}$ e $m$ ímpar. logo $m= 2k+1$ para algum $k \in \mathbb{Z}$.
$$
\begin{align*}
\frac{m}{2} + \frac{1}{2}&\\
\frac{2k+1}{2} + \frac{1}{2}&\\
\frac{2k+2}{2}&\\
\frac{2(k+1)}{2} &\\
k+1& 
\end{align*}
$$
Como $k \in \mathbb{Z}$, $k+1$ também pertence aos inteiros, portanto, a classe de equivalência de $\frac{1}{2}$ é $[\frac{1}{2} ]_{R} = \{\cdots, \frac{-3}{2}, \frac{-1}{2}, \frac{1}{2}, \frac{3}{2}, \frac{5}{2}, \cdots\}$, ou $\{\frac{m}{2} \text{ com }m \in \mathbb{Z} \mid m \text{ é impar e diferente de zero}\}$.
___
$\text{6 Questão}$

$D_{100} = \{1,2,4,5,10,20,25,50,100\}$
Diagrama de Hasse:
![[hasse.excalidraw]]

- *a)* maximais: $100$; minimais: $1$
- *b)* existe um máximo: $100$; existe um mínimo: $1$
- *c)* Limitantes superiores de $\{10,25\} \implies \{100\}$ 
- *d)* Supremo: $100$
- *e)* Limitantes inferiores de $\{10 ,100\}: \{1,2,4,5,10\}$
- *f)* Ínfimo de $\{10, 100\} \implies 10$
___
$\text{7 Questão}$

Primeiro par:
![[Drawing 2024-03-13 20.01.36.excalidraw]]
Checandos as invariantes, temos:
- Ambos **não** são bipartidos;
- Possuem $5$ vértices e $6$ arestas;
- Possuem $2$ vértices de grau $3$ e $3$ de grau $2$;
Então a função $\phi(G) \rightarrow H$ onde $G$ é o grafo da esquerda e $H$ o da direita é:
$$\begin{align*}
\phi(G) \rightarrow W=\begin{pmatrix}
A & B & C & D & E\\
3 & 1 & 2 & 4 & 1
\end{pmatrix}
\end{align*}$$
O Primeiro par é isormorfo.

O segundo grafo não é isomorfo pois o primeiro possui dois vértices de grau $2$ e o outro apenas $1.$
___
$\text{8 Questão}$

Suponha por contradição um grafo $G$ não conexo tal que $G$ possua $n \ge 3$ vértices e um número de arestas maior que $\frac{(n-1)(n-2)}{2}$. o número mínimo de arestas que um grafo conexo deve possuir é $n-1$. Portanto, devemos *provar ou desprovar* que $\frac{(n-1)(n-2)}{2} \lt n-1$ para $n \ge 3$
Para $n = 3$
$$\begin{align*}
\frac{(3-1)(3-2)}{2}\lt 2\\
\frac{2}{2}\lt 2\\
1 \lt 2
\end{align*}$$
Como $G$ tem *mais* do que $\frac{(n-1)(n-2)}{2}$ arestas, $G$, então, para $n=3$, tem *pelo menos* $2$ arestas, o que transforma a expressão em $2\lt2$, o que é falso, vamos demonstrar a falsidade do caso geral:
Assuma por contradição que é válido para $n=k$, portanto, seja $n = k+1$
$$\begin{align*}
\frac{((k+1)-1)((k+1)-2)}{2} &\lt (k+1)-1\\
\frac{k(k-1)}{2} &\lt k \\
k^{2}-k &\lt 2k\\
k^{2}&\lt 3k
\end{align*}$$
O que é sempre falso para $n \ge 3$. Portanto $G$ **deve** ser conexo.
___
$\text{9 Questão}$

Estamos falando de um grafo com $15$ vértices, *(os indivíduos)*, onde cada um tem exatamente três amigos. Sendo a amizade uma aresta entre dois vértices, dada vértice tem grau $3$, como há $15$ vértices, pelo teorema do aperto de mão:
$$\begin{align*}
2\cdot|E| &= 45\\
|E| &= \frac{45}{2}
\end{align*}$$
O grafo teria que possuir "$\frac{45}{2}$" arestas, o que é impossível, portanto este grafo não existe.
___
$\text{10 Questão}$

![[Pasted image 20240313212650.png]]
- Não possui circuito euleriano pois $c$ é ímpar.
- Possui caminho euleriano pois apenas $c$ e $a$ são ímpares, o caminho é, representado as arestas com pares: $(a,e), (e,b), (b,a), (a,f), (f,e), (e,c), (c,f), (f,d), (d,c)$.
- Ciclo hamiltoniano: $d,c,e,b,a,f,d$
- Caminho hamiltoniano: $d,c,e,b,a,f$.

![[Pasted image 20240313213247.png]]

- Não possui ciclo euleriano porque o grau de $0$ é ímpar.
- Não possui caminho euleriano pois existem mais do que dois vértices com grau ímpar: $0,1$ e $7$ por exemplo.
- Não possui ciclo hamiltoniano pois seria necessário ir e voltar pelo vértice $2$ para alcançar a segunda "porção" do grafo.
- Caminho hamiltoniano: $0,1,9,3,4,2,6,5,8,7,10$
___



*Desculpa pela formatação ruim, não consegui arrumar, o Obsidian não foi feito pra pdf's. :C*
