---
tags: matrix
---
Following the example provided in [[Elimination in Matrices]], after obtaining the [[Upper Triangular Matrix]], we can put it back in [[Definition of a System of Linear Equations|system]] form and solve it. See, our [[Matrix Definition|matrix]] was:
$A = \begin{bmatrix}1&2&1 \\ 0&2&-2 \\ 0 &0&5\end{bmatrix}$, if we let $b = \begin{bmatrix}2 \\ 6 \\ -10\end{bmatrix}$, to solve for $Ax=b$, we can build the system:
$$\begin{align*}
u=\begin{cases}
x+2y+z&= 2\\
2y-2z&= 6\\
5z&= -10
\end{cases}
\end{align*}$$
Notice we already know $z = -2$. now we **bubble up** our substitution to get $y= 1$ $x=2$.  
