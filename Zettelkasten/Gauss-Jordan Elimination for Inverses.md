---
tags: matrix
---
To properly find the [[Inverse Matrix]] of some **invertible** [[Matrix Definition|matrix]] $A$, we perform the Gauss-Jordan idea of elimination, it says that by performing the [[Elimination in Matrices|elimination]] on $A$ to find it's [[Row Echelon]] form, and simultaneously performing the same operations in a adjacent [[Identity Matrix]] $I$, if $A$ is indeed invertible, $A$ will turn into the identity, and $I$ will turn into the inverse. See:

$$\begin{align*}
\left[\begin{array}{c|c}
\begin{matrix}
1&3\\
2&7
\end{matrix}&
\begin{matrix}
1 & 0\\
0 & 1
\end{matrix}
\end{array}\right] \\
L_{2}\leftarrow L_{2} -2L_{1}
\\
\left[\begin{array}{c|c}
\begin{matrix}
1&3\\
0&1
\end{matrix}&
\begin{matrix}
1 & 0\\
-2& 1
\end{matrix}
\end{array}\right]\\
\\
L_{1}\leftarrow L_{1} -3L_{2}
\\
\left[\begin{array}{c|c}
\begin{matrix}
1&0\\
0&1
\end{matrix}&
\begin{matrix}
7 &-3\\
-2& 1
\end{matrix}
\end{array}\right]
\end{align*}$$
Here we see: the left side **is the identity** and this matrix on the right is the inverse of $A$, $A^{-1}$.