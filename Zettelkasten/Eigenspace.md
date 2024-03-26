---
tags: eigen-everything
---
Let $V$ be a [[Vector Space]], and $T$ be a [[Linear maps|linear map]], the set $E = \{ v \in V \mid T(v) = \lambda v\}$ which is the [[Union]] of the zero [[Vector]] with the set of all [[Eigenvalues and Eigenvectors|eigenvectors]] associated with a [[Eigenvalues and Eigenvectors|eigenvalue]] $\lambda$. $E$ is called the *eigenspace* or *characteristic space* of $T$ associated with $\lambda$. $E$ is a [[Linear Subspaces|subspace]] of course.
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