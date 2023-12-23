---
tags: matrix
aliases: permutation matrices, permutation matrix
---
It's a matrix $P_{kl}$ that [[Row Exchanges|exchanges]] rows $k$ and $l$ of a matrix $A$ when premultiplying.
The form of $P_{kl}$ can be done by exchanging the rows of a [[Identity Matrix]] of equal dimensions, $e.g.$
$$\begin{align*}
P_{23}&= \begin{pmatrix}1 & 0 & 0\\
0 & 0 & 1\\
0 & 1 & 0\end{pmatrix}
\end{align*}$$
With $k = 2$ and $l = 3$, Notice $P_{kl}^{-1}=P_{kl}$, since reversing the exchange process we just exchange the same rows again.