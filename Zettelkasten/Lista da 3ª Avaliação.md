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
1. $(a_{i},a-), $