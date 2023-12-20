---
tags: systems
---
Do [[Gaussian Elimination]] on a $Ax = b$ [[Definition of a System of Linear Equations|system]] creates a new system $Ux = c$, where $U$ is $A$ in [[Upper Triangular Matrix|upper triangular form]], $c$ is the new [[Vector|vector]] derived from $b$ by the same steps that took $A$ into $U$.
See an example:
$$\begin{align*}
Ax = \begin{pmatrix}
2 & 1 & 1\\
4 & 1 & 0\\
-2 & 2 & 1
\end{pmatrix}
\begin{pmatrix}
u\\
v\\
w\\
\end{pmatrix} = \begin{pmatrix}
1\\
-2\\
7\end{pmatrix}
\end{align*}$$
Then there's three elimination steps:
1. Subtract $2$ times the first equation from the second;
2. Subtract $-1$ times the first equation from the third (add);
3. Subtract $-3$ times the second equation from the third (add);
The result is the equivalent:
$$\begin{align*}
Ux = \begin{pmatrix}
2 & 1 & 1\\
0 & -1 & 0\\
0 & 0 & -4
\end{pmatrix}
\begin{pmatrix}
u\\
v\\
w\\
\end{pmatrix} = \begin{pmatrix}
1\\
-4\\
-4\end{pmatrix}
\end{align*}$$
There's the $Ux = c$. system.
The [[Matrix Definition|matrix]] $E$ that subtracts $2$ times the first equation from the second, denote it $E_{21}$ because it subtracts a multiple of equation $1$ from equation $2$, and also produces a zero in the $(2,1)$ position:
$$\begin{align*}
E_{21}=\begin{pmatrix}
1 & 0 & 0\\
-2 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
\end{align*}$$
The same can be done for steps $(2)$ and $(3)$:
$$
\begin{align*}
E_{31}=\begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
1 & 0 & 1
\end{pmatrix}\;\;
E_{32} = \begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 3 & 1
\end{pmatrix}
\end{align*}
$$
See that $E_{32}E_{31}E_{21}A$ turns $A$ into $U$ 
# How to Undo the Steps of $U$ ?

First notice that $E_{32}E_{31}E_{21}$ turns $A$ into $U$, so if we **reverse** the thing that $E_{32}E_{31}E_{21}$ does to $A$ to get it to $U$ we can find something to bring $U$ back to $A$, first, we have to **undo** the $E_{ij}$ step. Take $E_{21}$, *subtracts 2 times the first equation from the second*, so we have to undo this, by *adding 2 times the first equation to the second*, so:
$$\begin{align*}
E_{21}^{-1}&= 
\begin{pmatrix}
1 & 0 & 0\\
2 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
\end{align*}$$
Same for $E_{32}$ and $E_{31}$:
$$\begin{align*}
E_{31}^{-1}=\begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
-1 & 0 & 1
\end{pmatrix}\;\;
E_{32}^{-1} = \begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & -3 & 1
\end{pmatrix}
\end{align*}$$
Notice $E_{31}E_{31}^{-1}= I$, so one operation undoes the other.

An important thing is that we also need to reverse the order of the multiplications, since matrix [[Matrix Multiplication|multiplication]] isn't commutative. So the inverse would be $E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}$, so $A = E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}U$, Let $L = E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}$, so that $A = LU$, also $Lc = b$.

So $L = (E_{32}E_{31}E_{21})^{-1} \implies L^{-1}=E_{32}E_{31}E_{21}$.

$A$ = Original Matrix
$U$ = Upper triangular matrix obtained from [[Gaussian Elimination]].
$L$ = [[Lower Triangular Matrix]] that **undoes** $U$.

> [!important] Definition (kind of)
> As long as no [[Pivot|pivots]]  are zero, the matrix $A$ can be written as a product $LU$ of a lower triangular matrix $L$ and a upper triangular matrix $U$. The entries of $L$ on the main diagonal are $1$'s; below the diagonal, the are the multipliers $l_{ij}$ of row $j$ which are subtracted from row $i$ during elimination and before [[Back-Substitution]]; it's diagonal entries are the pivos.

