---
tags: matrix
---
Suppose two [[Matrix Definition|matrices]] $A_{1\times n}$ and $B_{n\times 1}$, multiplying these two, by the rules of [[Matrix Multiplication|multiplication]], would result in a single value, since each column of $A$ gets multiplying with each row of $B$ in column $1$ and summed up, So, for example, to get the value $C_{34}$ out of two $A$ and $B$ with arbitrary size $k$, do:
$$\begin{align*}
C_{34}&= (A_{3k})\cdot(B_{k4})\\
&= a_{31}b_{14}+a_{32}b_{24}+\cdots+a_{3k}b_{k4}&= \sum\limits_{k=1}^{n}a_{3k}b_{k4}
\end{align*}$$
