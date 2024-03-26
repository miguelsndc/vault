---
tags: eigen-everything
---
Let $V$ be a [[Vector Space]], and $T$ be a [[Linear maps|linear map]], the set $E = \{ v \in V \mid T(v) = \lambda v\}$ which is the [[Union]] of the zero [[Vector]] with the set of all [[Eigenvalues and Eigenvectors|eigenvectors]] associated with a [[Eigenvalues and Eigenvectors|eigenvalue]] $\lambda$. $E$ is called the *eigenspace* or *characteristic space* of $T$ associated with $\lambda$. $E$ is a [[Linear Subspaces|subspace]] of course.

The eigenspaces of $T$ always form a [[Direct sum of vector spaces|direct sum]]. As a consequence, eigenvectors of **different eigenvalues** are [[Linear (In)dependence.|linearly independent]]. Therefore the sum of the [[Theorems and Proofs for Basis and Dimension|dimensions]] of the eigenspaces **cannot exceed** the dimension $n$ of the space on which $T$ operates, and there cannot be more than $n$ distinct eigenvalues.
## Proof it's a subspace
- Closure under addition
Let $u, v \in E$, then:
$$\begin{align*}
T(u) &= \lambda u\\
T(v)&= \lambda v\\
T(u) + T(v) &= \lambda v + \lambda u\\
T(u+v) &= \lambda(u+v)
\end{align*}$$
Therefore $u + v \in E$.
- Closure under [[Scalar]] multiplication
Let $\alpha \in \mathbb{R}$ and $u \in E$, then:
$$\begin{align*}
T(u) &= \lambda u\\
\alpha T(u)&= \alpha\lambda u\\
T(\alpha u) &= \lambda(\alpha u)
\end{align*}$$
Therefore $\alpha u \in E$, so $E$ is a subspace.