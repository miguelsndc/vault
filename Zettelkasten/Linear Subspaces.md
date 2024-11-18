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
___
### Consequences and Derivations

Let $E$ be a [[Vector Space]], also let $F \subset E$, $F$ being a subspace of $E. Any [[Linear Combinations|linear combination]] of vectors $v_1, \cdots, v_n \in F$ also belongs to $F$. 
___
Let $v=(x_{1},x_{2},\cdots,x_{n})\in R^{n}$, let $a_{1},\cdots,a_{n}\in \R$, the set $H$ of all vectors $v$ is a **subspace**:
$$\begin{align*}
H &= \{ v=(x_{1},x_{2},\cdots,x_{n})\in R^{n} \mid a_{1}x_{1} + \cdots + a_{n}x_{n}=0\}
\end{align*}$$
When $a_{1}=a_{2}=\cdots=a_{n}=0$, the space spanned by $H$ is the entire $R^{n}$. since there are no restrictions to the vectors $H$ can reach. When at least one of the $a_{i} \ne 0$ we say that $H$ is a [[Hyperplanes|hyperplane]] of $R^{n}$ that passes through the origin.

