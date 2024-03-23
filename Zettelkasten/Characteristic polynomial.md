---
tags: eigen-everything
---
Let $A$ be a $n \times n$ [[Matrix Definition|matrix]]. From the definition of [[Eigenvalues and Eigenvectors]] we get the expression:
$$\begin{align*}
\det(A- \lambda I)&= 0\\
\det(
\begin{pmatrix}
a_{11}  & \cdots  & a_{1n}\\
\vdots\\
a_{n1}  & \cdots &  a_{nn}
\end{pmatrix}-
\begin{pmatrix}
  \lambda  & \cdots &  0\\
  \vdots\\
0 & \cdots & \lambda
  \end{pmatrix}
)&= \det(
\begin{pmatrix}
a_{11} - \lambda  & \cdots &  a_{1n}\\
\vdots\\
a_{n1} & \cdots & a_{nn} - \lambda
\end{pmatrix}
)
\end{align*}$$
$= (a_{11}-\lambda)^{e_{1}}(a_{22}-\lambda)^{e_{2}}\cdots$, the fol
