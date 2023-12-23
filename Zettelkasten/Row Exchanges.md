---
tags: systems, matrix
aliases: row exchange, row exchanges, exchange, exchanges
---
When doing [[Gaussian Elimination]] in a [[Matrix Definition|matrix]] for a [[Definition of a System of Linear Equations|system of linear equations]], in case encountering a zero [[Pivot|pivot]] in column $k$, if below column $k$, in a row $l$ let's say, there's a non-zero element, we can **exchange** rows $k$ and $l$ to avoid the zero pivot and allow elimination to proceed. this is done through [[Permutation Matrix]], See:
$$\begin{align*}
\begin{pmatrix}
0 & 2\\
3 & 4
\end{pmatrix}
\begin{pmatrix}u \\v\end{pmatrix} &= \begin{pmatrix}b_{1}\\ b_{2}\end{pmatrix}
\end{align*}$$**Zero pivot in $a_{11}$**, exchange rows $1$ and $2$.
$$\begin{align*}
\begin{pmatrix}
3 & 4\\
0 & 2\\
\end{pmatrix}
\begin{pmatrix}v \\u\end{pmatrix} &= \begin{pmatrix}b_{2}\\ b_{1}\end{pmatrix}
\end{align*}$$
Notice this also exhanges the [[Vector Matrix Form|column vector]], now $A$ is in [[Upper Triangular Matrix|upper triangular form]] and we can call it $U$, from [[A = LU Factorization]], $L$ is the [[Identity Matrix]].