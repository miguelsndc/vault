---
tags: spaces, systems, vector
aliases: linear dependent, linear independent, linearly independent, linear dependent, linear, linearly, dependent, independent
---
Given a set of vectors $v_{1},v_{2},\cdots, v_{k}$, we look at their [[Linear Combinations]]: $c_{1}v_{1}+c_{2}v_{2}+\cdots+c_{k}v_{k}$. The trivial combination $c_{i}=0$ produces the zero [[Vector|vector]], since $0v_{1}+0v_{2}+\cdots+0v_{k}=0$. The point is whether any other weights or [[Scalar|scalars]] also produce it.
___ 
If all non-trivial combinations of vectors are *non-zero*, $c_{1}v_{1}+c_{2}v_{2}+\cdots+c_{k}v_{k} \ne 0$, unless $c_{1}=c_{2}=\cdots=c_{k}=0$, then the vectors $v_{1},v_{2},\cdots,v_{k}$ are **Linearly Independent**. Otherwise they are **linearly dependent**, and one of them is a [[Linear Combinations|linear combination]] of the others.
$\rm{e.g.}$

> If one of the vectors, let's say, $v_{2}$, happen to be the zero vector, then we are certain that this combination is dependent. If we choose weights $c_{2}=4$ and $c_{i}=0$, this is certainly a nontrivial combination that yields the zero vector.

$\text{Ex 2:}$
Let $A$:
$$\begin{align*}
A&= \begin{pmatrix}
1  & 3 & 3 & 2\\
2 & 6 & 9 & 5 \\
-1 & -3 & 3 & 0
\end{pmatrix} \implies
\begin{pmatrix}
1 & 3 & 3 & 2\\
0 & 0 & 3 & 1\\
0 & 0 & 6 & 2
\end{pmatrix}
\end{align*}$$
Here we clearly see that row $3$ is a combination of the other rows, so $A$ has *linearly dependent rows*, we can also see dependent columns since column $2$ is three times column $1$.

The rows of the $n\times n$ [[Identity Matrix]] $I$:
$$\begin{align*}
I&= \begin{pmatrix}
1 & 0 & 0 & \cdot\\
0 & 1 & 0 & \cdot\\
0 & 0 & \cdot & 0\\
\cdot & \cdot & 0 & 1
\end{pmatrix}
\end{align*}$$
Are linearly independent. We give this vectors a special notation $e_{1},e_{2},\cdots, e_{n}$, they are the unit vectors in the coordinate directions, $e_{1}=(1,0,0,\cdots,0)$, $e_{n}=(0,0,\cdots,1)$.
## Procedure for Proving Independence
Assume that the linear combination gives zero, and prove that all weight $c_{i}$ must equal zero, for example:
$$\begin{align*}
c_{1}e_{1}+ c_{2}e_{2}+\cdots+c_{n}e_{n}=(c_{1},c_{2},\cdots, c_{n})\\
\end{align*}$$
If the combination is the zero vector then obviously all $c_{i}=0$.
$\rm{e.g.}$
>Suppose $U$ is an $n\times n$ [[Upper Triangular Matrix]], with non-zero [[Pivot|pivots]] in the diagonal. Then the rows of $U$ are linearly independent.

*Proof:*
We start by assuming that some linear combination of the rows is zero, $c_{1}v_{1}+c_{2}v_{2}+\cdots+c_{k}v_{k}=0$. Then we head for the first non-zero entry in the diagonal $u_{11}$, since we know $c_{1}v_{1}=0$ and $v_{1}\ne 0$, this implies that $c_{1}=0$, and $c_{2}=0$ since $c_{1}v_{1}+ c_{2}v_{2}=0$ and $v_{2}\ne 0$, this applies to all $u_{ij}$ pivots, since the only weights that make $c_{1}v_{1}+c_{2}v_{2}+\cdots+ c_{k}v_{k}=0$ are those of the trivial solution. Then $U$ is linearly independent.
___
The $r$ nonzero rows of an [[Echelon Form|echelon]] matrix $U$ are linearly independent, and so are the $r$ columns that contain nonzero pivots.
$\rightarrow$ An important reminder is that the definition of linear independence is "coordinate free". Given $k$ points in $n$-dimensional space, the vectors from the origin to those points either can or cannot be combined to give zero, regardless of where we put the coordinate axes. A rotation will change the coordinates however it won't affect the question of dependent or independent whatsoever.
$\rightarrow$ Given an arbitrary [[Sets|set]] of vectors, their 
