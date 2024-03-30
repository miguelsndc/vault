---
tags: eigen-everything
---
The proposition is in the title, the proof goes as follows:
Let $V$ be a [[Vector Space|vector space]]. If $A$ is a [[Diagonalizable Matrices|diagonalizable]] [[Matrix Definition|matrix]], then there exists some [[Theorems and Proofs for Basis and Dimension|basis]] $\gamma$ of $V$ where $[A]^{\gamma}_{\gamma}$ is:
$$\begin{align*}
\begin{pmatrix}
\lambda_{1} & 0 & \cdots & 0\\
0 & \lambda_{2} & \cdots & 0\\
\vdots  & \vdots &   & \vdots\\
0 & 0 & \cdots & \lambda_{n}
\end{pmatrix}
\end{align*}$$
Therefore $\det{[A]^{\gamma}_{\gamma}}=  \prod_{i=1}^{n}\lambda_{i}$. Now let $\alpha$ be a arbitrary basis of $V$, then:
$$\begin{align*}
[A]^{\alpha}_{\alpha}=[I]^{\gamma}_{\alpha}\cdot [A]^{\gamma}_{\gamma}\cdot [I]^{\alpha}_{\gamma}
\end{align*}$$
Let $P = [I]^{\gamma}_{\alpha}$, therefore:
$$\begin{align*}
[A]^{\alpha}_{\alpha}&= P\cdot [A]^{\gamma}_{\gamma}\cdot P^{-1}\\
\det{[A]^{\alpha}_{\alpha}}&= \det(P\cdot [A]^{\gamma}_{\gamma}\cdot P^{-1})\\
&= \det(P) \cdot \det([A]^{\gamma}_{\gamma}) \cdot \det(P^{-1})\\
&= \det(P\cdot P^{-1}) \cdot \det([A]^{\gamma}_{\gamma})\\
&= \det(I) \cdot \det([A]^{\gamma}_{\gamma})\\
&=  \det([A]^{\gamma}_{\gamma})\\
&= \prod_{i=1}^{n}\lambda_{i}
\end{align*}$$
So it's proven that regardless of the [[Theorems and Proofs for Basis and Dimension|basis]] $A$ is written in, if $A$ is diagonalizable, the determinant of $A$ is the product of it's [[Eigenvalues and Eigenvectors|eigenvalues]].