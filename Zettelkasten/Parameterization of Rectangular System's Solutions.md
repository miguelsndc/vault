---
tags: systems, spaces, matrix
aliases: parameterization
---
With $Ax=b$ [[Definition of a System of Linear Equations|system]], by trying to read off the solutions we come across some cases, consider the homogeneous case: $Ax=0$ for the following [[Definition of a System of Linear Equations|system]]:
$$\begin{align*}
Ux&=
\begin{pmatrix}
1 & 3 & 3 & 2\\
0 & 0 & 3 & 1\\
0 & 0 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
u\\ v \\ w \\ y
\end{pmatrix}
&= 
\begin{pmatrix}
0\\ 0 \\ 0 \end{pmatrix}
\end{align*}$$
Here the unknowns fall into two categories, **basic variables**: *(columns with non-zero [[Pivot|pivots]])*, first and third columns in this case, so $u$ and $w$ are our basic variables.
The other category is made of **free variables**, *(columns with zero [[Pivot|pivots]])*, second and fourth columns, so $v$ and $y$ are our free variables.
To find a general solution for this we may assign arbitrary values, the so called **parameters**, to $v$ and $y$, our **free variables**, See:
$$\begin{align*}
u+3v+3w+2y 
\end{align*}$$