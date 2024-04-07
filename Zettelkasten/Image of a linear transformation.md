---
tags: linear-transformations
aliases: image, column space
---
Let $T:V \rightarrow W$ be a [[Linear Transformations|linear transformation]] over two [[Vector Space|vector spaces]] $V$ and $W$. then the *image of $T$* denoted $\im(T)$ is a [[Subsets|subset]] of $W$ and is made of all vectors in $V$ that are transformed by $T$, $\im(T) \subset W$.
Definition:
$$\begin{align*}
\im(T) &= \{w \in W \mid w = T(v)\} \text{ for some } v\in V
\end{align*}$$
> Theorem: if $T$ is a [[Linear Transformations|linear transformation]] then the image $\im(T)$ is a [[Linear Subspaces|subspace]].
## Proof
1. Let $w_{1},w_{2} \in \im(T)$ we want to prove $w_{1}+w_{2}\in \im(T)$, so by the definition $w_{1}=T(v_{1})$ and $w_{2}= T(v_{2})$ for some $v_{1}, v_{2} \in V$, by the properties of [[Linear Transformations]] $w_{1}+w_{2}=T(v_{1})+T(v_{2})=T(v_{1}+v_{2})$. notice $T(v_{1}+v_{2})\in \im(T)$ therefore $\im(T)$ is closed under addition.
2. Let $w_{2} \in \im(T)$ this implies that $w_{1}=T(v_{1})$. for some $v_{1}\in V$, let also $\lambda \in \mathbb{R}$, then $\lambda w_{1}=\lambda T(v_{1})$, since $T$ is a [[Linear Transformations|transformation]], $\lambda T(v_{1})=T(\lambda v_{1}) \implies T(\lambda v_{1}) \in \im(T)$ therefore the image is closed under scalar multiplication.
___
## How to find it
Recall by the definition that $\im(T) = \{w \in W \mid T(v) = w, v\in V\}$, to describe the image either as a [[Homogeneous System]] or as a [[Span|spanning set]], we apply a generic vector $(x_{1},x_{2},\cdots,x_{n})$ on a transformation $T$ and let it equals another generic vector $y_{1},y_{2},\cdots, y_{n}$ on the [[Domain]] and based on the rules of $T$ we define $y_{1},y_{2}, \cdots, y_{n}$ as [[Linear Combinations]] of the coefficients of $x_{i}$, then we can find a [[Theorems and Proofs for Basis and Dimension|basis]] for something like that.
Example:
Let $T:P_{2}\rightarrow R^{2}\mid T(a_{0} + a_{1}X + a_{2}X^{2})=(2a_{0} - a_{1}+a_{2}, 2a_{0}+3a_{1}+5a_{2})$, now we set a generic vector from the [[Domain]] to a generic vector on the [[Image of a linear transformation|image]], $T(a_{0}+a_{1}X+ a_{2}X^{2})=(x,y)$, now replace $T$ with it's rules, $(2a_{0}-a_{1}+a_{2},2a_{0}+3a_{1}+5a_{2})=(x,y)$, now express it as combinations of the coefficients of $P_{2}$: $a_{0}(2,2) + a_{1}(-1,3)+a_{2}(1,5)=(x,y)$. Therefore $\im(T) = [(2,2), (-1,3), (1,5)]$. We can check for [[Linear (In)dependence.|linear dependence]], and after a quick check the image becomes $\im(T) = [(1,0), (0,1)]=\mathbb{R}^{2}$.