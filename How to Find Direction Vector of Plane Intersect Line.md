---
tags:
  - avlc
aliases: 
date: 2023-11-16
---
To find the direction [[vault/content/S1/AVLC/Vector|vector]] of a [[Plane Intersect Line]] $r$. you need to solve a **determinant** with the coefficients of the line, see:
$$\begin{align*}
r: \begin{cases}
x-z=3\\
2y+3z+1=0
\end{cases}\\\\
\begin{bmatrix}
i&j&k\\
1&0&-1\\
0&2&3
\end{bmatrix}
\end{align*}$$
Solving the determinant for the above matrix we'll have the coordinates of the direction vector based on the [[Canonical Vectors]], and then you can arbitrate values for $x$ or any other axis to figure out a point and build a [[Parametric Line Equation|parametric line]] from it.