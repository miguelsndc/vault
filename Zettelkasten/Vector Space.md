---
tags: spaces
aliases: vector space, vector spaces, space, spaces
---
A **Vector Space** is a collection, a bunch of [[Vector|vectors]], a [[Sets|set]], so to say, that obbey certain rules of addition and [[Multiplication by Scalar]]. $\text{e.g.}$ 
$$\begin{align*}
R^{2}&= \Big\{ \begin{pmatrix}x \\ y\end{pmatrix} \mid x,y\in\mathbb{R} \Big\} 
\end{align*}$$
There's eight **axioms** that a collection of vectors must obbey in order to be considered a vector space:
1.  Associativity of vector addition:
$$\begin{align*}
\vec{u} + (\vec{v} + \vec{w}) &= (\vec{u} + \vec{v}) + \vec{w}
\end{align*}$$
2. Commutativity of vector addition:
$$
\begin{align*}
\vec{u} + \vec{v} &= \vec{v} + \vec{u}
\end{align*}
$$
3. Identity Element* of vector addition:
	There exists an element $\mathbf{0} \in V$, called the **zero vector** such that $\vec{v} + 0 = \vec{v}$ for all $\vec{v} \in V$.
$$\begin{align*}
\exists\mathbf{0}\in V \text{ s.t. } \forall \vec{v} \in V \mid\vec{v} + \mathbf{0}=\vec{v} 
\end{align*}$$
4. *Inverse elements* of vector addition:
$$\begin{align*}
\forall \vec{v} \in V \;\exists(\mathbf{-\vec{v}})\in V \text{ (called the additive inverse of $\vec{v}$) } \text{ s.t. } \vec{v}+(-\vec{v}) &= \mathbf{0}
\end{align*}$$
5. Compatibility of Scalar Multiplication with Field Multiplication
$$\begin{align*}
a(b\vec{v})=(ab)
\end{align*}$$