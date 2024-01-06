---
tags: spaces
aliases: subspace, subspaces, linear subspace
---
A Vector **sub**space is a [[Subsets|subset]] of a [[Vector Space]] that is, in itself, a vector space. All the [[Eight Axioms for Vector Spaces|eight axioms]] are already fulfilled by the superset (the vector space in which the subspace is contained). So for a subset to be a subspace, it needs to account for:

- Must contain the Zero Vector $\mathbf{0}$. *(Non-emptyness)*
- Closure under Addition:
$$\begin{align*}
\forall\vec{v}\forall\vec{u}\in V,(\vec{u}+\vec{v})\in V
\end{align*}$$
- Closure under [[Multiplication by Scalar|scalar multiplication]]:
$$\begin{align*}
\forall a\in \mathbb{R},\forall\vec{v}\in V,a\vec{v}\in V
\end{align*}$$
A Interesting fact is that the Zero Vector itself is a subspace, since $\mathbf{0} + \mathbf{0} = \mathbf{0}$ and $\forall a \in \mathbb{R}, a\mathbf{0} = \mathbf{0}$.
