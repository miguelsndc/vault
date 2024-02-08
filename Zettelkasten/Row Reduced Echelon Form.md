---
tags: systems
aliases: row reduced
---
Row reduced echelon form is very similar to the regular [[Echelon Form]], however, in this case, ***every column that contains a pivot must be made all of zeroes and the pivot must be one***. as such:
$$\begin{align*}
\begin{pmatrix}
1  & 0 & 0 & *\\
0 & 1 & 0 & *\\\
0 & 0 & 1 & *
\end{pmatrix}
\end{align*}$$
If the [[Rank of a Matrix|rank]] is greather than the number of equations, then one row must be zero-only.