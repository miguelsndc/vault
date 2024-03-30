---
tags: eigen-everything, matrix
aliases: diagonalizable
---
Let $V$ be a [[Vector Space]], Let $T$ be a [[Linear maps|linear map]] in $V$. Then , $T$ is *diagonalizable*, that is, can be written as a matrix where:
$$\begin{align*}
\begin{cases}
T_{ij}&= 0; \;\; i\ne j\\
T_{ii}&= \lambda_{i}
\end{cases}
\end{align*}$$
Where each diagonal element is a [[Eigenvalues and Eigenvectors|eigenvalue]] of $T$. Since [[Eigenvectors with distinct Eigenvalues are linearly independent]], it follows that if we have as many *distinct eigenvalues* as the [[Theorems and Proofs for Basis and Dimension|dimension]] of the space, it's possible to form a [[Theorems and Proofs for Basis and Dimension|basis]] of $V$ consisting exclusively of the eigenvectors of $T$.
___
Given an arbitrary [[Linear Transformations|transformation]] $T: V \rightarrow V$, if we accomplish to find a basis $\beta = \{v_{1}, v_{2}, \cdots, v_{n} \}$, where each $v_{i}$ is an eigenvector of $T$, since:
$$
\begin{align*}
T(v_{1})& = \lambda_{1}\cdot v_{1}+ 0\cdot v_{2}+\cdots+0 \cdot v_{n}\\
T(v_{2})& = 0 \cdot v_{1}+ \lambda_{2}\cdot v_{2}+\cdots+0 \cdot v_{n}\\
\vdots\\
T(v_{n})&=  0 \cdot v_{1}+ 0\cdot v_{2}+\cdots+ \lambda_{n}\cdot v_{n}\\
\end{align*}
$$
The [[Vector Coordinates|coordinates]] of each [[Vector|vector]] of this [[Theorems and Proofs for Basis and Dimension|basis]] is it's own eigenvalue. Since each column of the matrix is formed by the coordinates of each column vector on the specified basis, $T$ will be a *diagonal* [[Matrix Definition|matrix]], where each element of the main diagonal are the eigenvalues $\lambda_{i}$ of $T$.
$$\begin{align*}
[T]^{\beta}_{\beta}&= 
\begin{pmatrix}
\lambda_{1} & 0 & \cdots & 0\\
0 & \lambda_{2} & \cdots &0\\
\vdots & \vdots  & & \vdots\\
0  & 0 & \cdots & \lambda_{n}
\end{pmatrix}
\end{align*}$$
It's not necessarily required that all the $\lambda_{i}$ eigenvalues are *distinct*, actually, an eigenvalue will appear in the main diagonal as many times as there is [[Linear (In)dependence.|linearly independent]] [[Eigenvalues and Eigenvectors|eigenvectors]] associated to it. 
If there exists a basis $\gamma = {u_{1}, u_{2}, \cdots, u_{n}}$ of $V$ such that:
$$\begin{align*}
[T]^{\gamma}_{\gamma}=
\begin{pmatrix}
a_{1} & 0 & \cdots & 0\\
0 & a_{2} & \cdots &0\\
\vdots & \vdots  & & \vdots\\
0  & 0 & \cdots & a_{n}
\end{pmatrix}
\end{align*}$$
Then notice that $u_{1}, \cdots, u_{n}$ **are the [[Eigenvalues and Eigenvectors|eigenvectors]]** of $T$ with eigenvalues $a_{1}, \cdots, a_{n}$, respectively.