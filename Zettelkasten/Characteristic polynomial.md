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
$= (a_{11}-\lambda)^{e_{1}}(a_{22}-\lambda)^{e_{2}}\cdots$, the [[Polynomials|polynomial]] that comes up when calculating the [[Determinant]] of $A - \lambda I$ is called the **characteristic polynomial** $P(\lambda)$ of $A$ and it's roots are the [[Eigenvalues and Eigenvectors|eigenvalues]] of $A$.
*$A$ has real eigenvectors and eigenvalues if and only if $P(\lambda)$ has real roots*. However, when working with [[Complex Numbers|complex]] [[Vector Space|vector spaces]], since polynomials always have complex roots, $A$ will always have both eigenvalues and vectors.
