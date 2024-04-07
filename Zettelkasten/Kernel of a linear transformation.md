---
tags: linear-transformations
aliases: kernel, null space
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
___
## How to find it
By the definition $\nu(T)$ is all $T(v) = \vec{0}$, to find it, set every rule of the [[Linear Transformations|transformation]] to $0$ and you have a [[Linear Subspaces|subspace]] defined by a [[Homogeneous System]], you might want to check for [[Linear (In)dependence.|linear dependence]] or find a [[Span]]ning set, but that's trivial. Example:
Let $T:\mathbb{R}^{2}\rightarrow\mathbb{R}^{3} \mid T(x,y)=(x+y, x-y, x-y)$, then $\nu(T)=\{(x,y) \in \mathbb{R}^{2} \mid T(x,y) = (0,0,0)\}$, therefore we have: $(x+y, x-y, x-y) = (0,0,0)$ which forms: $\begin{cases} x+y=0\\ x-y = 0 \end{cases} \therefore \nu(T)= \{\vec{0}\}$. 


