---
tags: linear-transformations
---
The Kernel of a [[Linear Transformations]] $T: V \rightarrow W$ are those vectors from $V$ that are mapped to the **origin of $W$** denoted $\nu(T) or \ker(T)$. The definition is:
$$\begin{align*}
\nu(T)&= \{v \in V \mid T(v) = \vec{0}\}
\end{align*}$$
The Kernel is also a [[Linear Subspaces|subspace]], since it preserves addition and [[Multiplication by Scalar|scalar multiplication]], this can be easily shown, and, since it's a subspace, it can be written as a [[Homogeneous System]].
Let $T: V \rightarrow W$ be a [[Linear Transformations]], $U$ and $V$ [[Vector Space|vector spaces]].
1. Closure under addition:
Let $u,v \in \nu(T)$, Since $T(u) = \vec{0}$ and $T(v) = \vec{0}$, then $T(u+v) = T(u) + T(v) = \vec{0} + \vec{0} = \vec{0}$.
2. Closure under scalar multiplication:
Let $\lambda \in \mathbb{R}$, $u \in \nu(T)$, then $T(u) = \vec{0}$, so $\lambda T(u) = \lambda \vec{0}$, so $\lambda T(u) = \vec{0}$ and since $\lambda T(u) = T(\lambda u)$, $\nu(T)$ is closed under *s.m*.