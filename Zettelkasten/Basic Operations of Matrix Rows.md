---
tags: matrix
---
Here we state the three elementary operations in the rows of a [[Matrix Definition|matrix]], Let $L_{i}$ represent the $i$th row in a arbitrary matrix.

1. Permutation of the $i$th and $j$th rows. $(L_{i} \leftrightarrow L_{j})$.
*Example: $L_{2} \leftrightarrow L_{3}$*
$$
\begin{bmatrix}
8 & 6 \\
1 & 3 \\
9 & 2 \\
\end{bmatrix}
\Rightarrow
\begin{bmatrix}
8 & 6 \\
9 & 2 \\
1 & 3 \\
\end{bmatrix}
$$
2. Multiplication of the $i$th row by a non-null [[Scalar|scalar]] $k$. $(L_{i}\rightarrow kL_{i})$
*Example: $L_{2}\rightarrow -3L_{2}$*
$$
\begin{bmatrix}
2 & 5 \\
3 & 7 \\
1 & 4 \\
\end{bmatrix}
\Rightarrow
\begin{bmatrix}
2 & 5 \\
-9 & -21 \\
1 & 4 \\
\end{bmatrix}
$$
3. Replace the $i$th row by the $i$th row plus $k$ times the $j$th row: $(L_{i} \rightarrow L_{i}+kL_{j})$, It's like a combination of properties $1$ and $2$.
*Example:*