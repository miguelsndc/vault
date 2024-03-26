---
tags: eigen-everything
---
Let $\lambda_{i}$ be an [[Eigenvalues and Eigenvectors|eigenvalue]] of a $n \times n$ [[Matrix Definition|matrix]] $A$. The *algebraic multiplicity* $\mu_{A}(\lambda_{i})$ it's the largest integer $k$ such that $(\lambda - \lambda_{i})^{k}$ divides evenly the [[Characteristic polynomial]] of $A$.

Suppose a matrix $A$ has [[Theorems and Proofs for Basis and Dimension|dimension]] $n$ and $d \le n$ distinct [[Eigenvalues and Eigenvectors|eigenvalues]]. The [[Characteristic polynomial]] of $A$ can be written as a product of the $d$ terms, each corresponding to a distinct eigenvalue raised to it's algebraic multiplicity.
$$\begin{align*}
\det(A - \lambda I) &= (\lambda_{1} - \lambda)^{\mu_{A}(\lambda_{1})}(\lambda_{2} - \lambda)^{\mu_{A}(\lambda_{2})} \cdots (\lambda_{d} - \lambda)^{\mu_{A}(\lambda_{d})}
\end{align*}$$
The algebraic multiplicity of each eigenvalue is related to the dimension as:
$$\begin{align*}
1 &\le \mu_{A}(\lambda_{i}) \le n\\
\mu_{A}&= \sum_{i=1}^{d} \mu_{A}(\lambda_{i})=n
\end{align*}$$