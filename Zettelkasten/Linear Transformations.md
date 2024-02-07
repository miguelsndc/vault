---
tags: linear-transformations
---
Let $V$ and $U$ be [[Vector Space|vector spaces]], and a "mapping" $A: E \rightarrow F$ is called *a **linear transformation*** if:
- $A(u+v) = A(u) + A(v)$
- $A(ku) = k\cdot A(u)$ 
$\forall v,u \in E, \forall k \in \mathbb{R}$.
We need both addition and [[Multiplication by Scalar|scalar multiplication]] to be preserved under transformations. The origin must also be preserved, because:
$$\begin{align*}
T(\vec{0})=\vec{0} \because T(0 \cdot v)=0 \cdot T(v)&= 0\\
\therefore T(\vec{0})&= \vec{0}
\end{align*}$$
Seeing if the origin is preserved might be a quick shortcut for checking whether a [[Functions in Discrete Math|function]] is a valid linear transformation or not.