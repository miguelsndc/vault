---
tags: matrix
aliases: transpose
---
The *transpose* of a [[Matrix Definition|matrix]] $A$ is obtained when the rows become the columns, and the columns become the rows. denoted $A^{T}$. $e.g.$
$$\begin{align*}
\begin{pmatrix}
1 & 3 & 2\\
2& 1 & 5\\
1 & 2 & 3
\end{pmatrix}^{T}=
\begin{pmatrix}
1 & 2 & 1\\
3 & 1 & 2\\
2 & 5 & 3
\end{pmatrix}
\end{align*}$$
The $i$th row of $A$ becomes the $i$th column of $A^{T}$. Tranposition can also be seen as "fliping $A$ over the diagonal".
## Properties
 - The transpose of the transpose is the matrix itself:
 $$\begin{align*}
(A^{T})^{T} &= A
\end{align*}$$
- The transpose of a [[Matrix Multiplication|multiplication]] is the transpose of each matrix in reverse order:
$$\begin{align*}
(AB)^{T}=B^{T}A^{T}
\end{align*}$$
- By multiplying a nonsquare matrix by its transpose, we obtain a [[Symmetric Matrix]}.
- Symmetric matrices $S$ are equal to their transpose, $S^{T} = S \implies \text{S is Symmetric}$.