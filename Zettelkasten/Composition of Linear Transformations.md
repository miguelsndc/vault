---
tags: linear-transformations
---
Consider two [[Linear Transformations]] $T:V \rightarrow W$ and $S:W\rightarrow U$, the *composition of $S$ with $T$*, $S\circ T$, is defined as $S \circ T : V \rightarrow U$, $S(T(v)), v \in V$. The concept works similarly to [[Composite Functions]].

> Proposition: Let $S$ and $T$ be linear transformations, then $S\circ T$ is a [[Linear Transformations|linear transformation]]. 
## Proof
1. $S\circ T (u+v) = S\circ T(u) + S \circ T(v) \implies S(T(u+v))= S(T(u) + T(v))$, since $T$ is a linear transformation. $S(T(u) + T(v)) = S(T(u)) + S(T(v))$, since $S$ is a linear transformation, hence $S\circ T(u+v) = S\circ T(u) + S\circ T(v)$.
2. $S\circ T(ku) = k\cdot S\circ T(u)$. $S\circ T(ku) = S(T(ku))$, since $T$ is linear, $S(T(ku)) = S(kT(u)).$ Since $S$ is linear, $S(kT(u)) = kS(T(u))$. Therefore $S\circ T(ku) = k\cdot S\circ T(u)$.
___
The procedure for finding the composite of two transformations is quite straightfoward, just plug the expressions of the **inner-most** transformations into the **outer**. Notice the [[Range]] of the inner must match the [[Domain]] of the outer.
## Examples
*Let $S:\mathbb{R}^{2}\rightarrow \mathbb{R}^{3}$ given by $S(x,y)=(x+y,x-y,2y)$ and let $T:R^{3}\rightarrow R^{2}$ given by $T(x,y,z) = (x+y+z, 2x-z)$. Find the expression of $S\circ T$.*

The definition of [[Composition of Linear Transformations]] is that $S\circ T = S(T(v))$. So since the [[Range]] of the inner match the [[Domain]] of the outer. The composition exists. Therefore:
$$\begin{align*}
S \circ T &= S(T(x,y,z))\\
&= S((x+y+z) + (2x-z), (x+y+z) - (2x-z), 2(2x-z))
\end{align*}$$
Treat every expression in the inner as a coordinate of the outer. and **plug in**.
$$\begin{align*}
S \circ T&=  ((x+y+z) + (2x-z), (x+y+z) - (2x-z), 2(2x-z))\\
&= (3x+y,-x+y+2z,4x-2z) 
\end{align*}$$
From now on it's just a regular transformation, we can find [[Kernel of a linear transformation|kernel]], [[Image of a linear transformation|image]], [[Theorems and Proofs for Basis and Dimension|basis]] and all that. One thing to notice about the kernel and the image of a composite transformation is that:
$$\begin{align*}
T:V \rightarrow W\\
S:W \rightarrow U\\
\nu(S\circ T) \supseteq \nu(T)\\
\im(S \circ T) \subseteq \im(T)
\end{align*}$$
The kernel of $T$ is taking all vectors to the $\vec{0}$ on $W$, and then being taken to the $\vec{0}$ in $U$. However, there might be some vectors, not in $\nu(T)$ that get taken from $W$ to the zero in $U$.
But $\im(S\circ T)$ cannot be larger than $\im(S)$, but it can be equal or smaller, so its **contained** in $\im(S)$.







