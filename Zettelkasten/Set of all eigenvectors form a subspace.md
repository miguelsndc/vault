---
tags: eigen-everything
---
The [[Sets|set]] of all [[Eigenvalues and Eigenvectors|eigenvectors]] of a given [[Linear Transformations|transformation]] $T:V \rightarrow V$ [[Span|span]] a [[Linear Subspaces|subspace]] of $V$.
Let $V_{\lambda}= \{v \in V \mid T(v) = \lambda v, \lambda \in \mathbb{R}\}$ be that [[Sets|set]].
- Closure under addition
Let $u,v \in V$, then:
$$\begin{align*}
T(u) + T(v) &= \lambda u + \lambda v\\
T(u+v)&= \lambda u + \lambda v\\
T(u+v)&= \lambda(u+v)
\end{align*}$$
- Closure under [[Scalar|scalar]] multiplication
Let $u \in V_{\lambda}$, then:
$$\begin{align*}
T(u) &= \lambda u\\
\alpha T(u)&= \alpha \lambda u , \;\; \alpha \in \mathbb{R}\\
T(\alpha u)&= \lambda(\alpha u)
\end{align*}$$
Hence $V_\lambda$ is a [[Linear Subspaces|subspace]].

