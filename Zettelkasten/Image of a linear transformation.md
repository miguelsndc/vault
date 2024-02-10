---
tags: linear-transformations
aliases: image
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
Recall by the definition that $\im(T) = \{w \in W \mid T(v) = w, v\in V\}$.