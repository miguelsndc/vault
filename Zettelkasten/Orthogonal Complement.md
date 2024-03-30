---
tags: vector, spaces
---
Let $V$ be a [[Vector Space]] with [[Inner Product|inner product]] $\innp{,}$ and let $S \subset V$ non-empty,  *(S isn't necessarily a [[Linear Subspaces|subspace]])*. The orthogonal complement of $S$, $S^\perp$ is the [[Sets|set]] of all [[Vector|vectors]] that are [[Orthogonality|orthogonal]] to all vectors in $S$, denoted:
$$\begin{align*}
S^{\perp}=\{v \in V \mid \innp{v,w}=0\;\;, w\in S\}
\end{align*}$$
Even though $S$ might not be a subspace, $S^{\perp}$ is, see:

- Let $v_{1},v_{2}\in S^{\perp}$ and $v \in S$, so $v_{1}\perp v$ and $v_{2} \perp v$, from the properties defined in [[Orthogonality]], $v_{1}+ v_{2}\perp v$.
- Let $\alpha \in \R$, let $v_{1} \in S^{\perp}$ and $v \in S$. $\alpha v_{1} \perp v$ trivially.

Therefore $S^{\perp}$ is a [[Linear Subspaces|subspace]].+
