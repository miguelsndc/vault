$\text{1 Questão}$:
$A = \{2,3,4,5,6,7,8\}$.
$xRy \iff x-y =3n$ para $n \in \mathbb{Z}$.
## *Verificando se é uma Relação de Equivalência*:
1. Reflexividade
   Seja algum $a \in A$, o par $(a,a) \in R$ se $a-a = 3n$, o que se traduz em $0 = 3n$, e que é verdade para $n=0$, logo $R$ é reflexiva.
2. Simetria
   Seja $(a,b)$ tal que $a-b = 3n$ e $a \gt b$. 
   Assume-se $a \ne b$ pois se $a = b$, pela reflexividade, tem-se que $(a,a) \in R$.
   Portanto o bar $(b,a)$ será tal que $b - a = -3n$, que é igual a $3(-n)$. Logo, para todo $n$ que satisfaz $(a,b)$, $-n$ satisfará $(b,a)$. Caso assumíssemos $a \lt b$, a demonstração é análoga, com a conclusão invertida.
3. Transitividadade
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
- Reflexividade:
  Seja $a \in R$, então $(a,a) \in R \iff a-a \in \mathbb{Z}$, porém como $a-a=0$ e $0 \in \mathbb{Z}$, $(a,a) \in R$.
  Portanto, $R$ é reflexiva.