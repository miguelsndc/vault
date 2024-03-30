---
tags: spaces, linear-transformations, vector
aliases: inner product, inner products, inner
---
The *inner product* over some [[Vector Space|vector space]] $V$ is a [[Functions|function]] that maps every pair of [[Vector|vectors]] $v, w \in V$  to a [[Real Numbers|real number]], denoted $\innp{u, w}$. $\innp{,} = V \times V \rightarrow \mathbb{R}$. It's the generalization of the concepts involving measure for $n$-dimensional space.
## Axioms
- $\innp{v, v} \ge 0 \;\; \forall v \in V$. also $\innp{u,v}= 0 \iff v = \vec{0}$;
- $\innp{\alpha v, v} = \alpha \innp{v,v}$, for all $\alpha \in \mathbb{R}$;
- $\innp{v_{1} + v_{2}, v_{3}} = \innp{v_{1}, v_{3}} + \innp{v_{2}, v_{3}}$;
- $\innp{v_{1},v_{2}} = \innp{v_{2}, v_{1}}$.
  
The [[Scalar Product|dot product]] itself satifies these properties and therefore is a *inner product*, having a special name: The *usual* inner product. But any function that satisfy the axioms will be a valid inner product, Examples are:

Let $V$ be the space of [[Differentiability and Continuity|continuous]] functions in the [[Intervals|interval]] $[0,1]$. Given $f_{1}, f_{2}\in V$:
$$\begin{align*}
\innp{f_{1},f_{2}}=\int_{0}^{1} f_{1}(t)f_{2}(t) dt\\
\end{align*}$$
Is a inner product, proof:
- $\innp{v, v} \ge 0 \;\; \forall v \in V$. also $\innp{u,v}= 0 \iff v = \vec{0}$;
$$\begin{align*}
\innp{p(x), p(x)} &= \int_{0}^{1}p^{2}(x) \, dx \ge 0
\end{align*}$$
- $\innp{\alpha v, v} = \alpha \innp{v,v}$, for all $\alpha \in \mathbb{R}$;
$$\begin{align*}
\innp{\alpha p(x), p(x)} &= \int_{0}^{1}\alpha p^{2}(x) \, dx\\
&= \alpha \int_{0}^{1}p^{2}(x) \, dx\\
&= \alpha \innp{p(x), p(x)}
\end{align*}$$

- $\innp{v_{1} + v_{2}, v_{3}} = \innp{v_{1}, v_{3}} + \innp{v_{2}, v_{3}}$;
$$\begin{align*}
\innp{p(x) + q(x), r(x)} &= \int_{0}^{1}(p(x)+q(x))r(x) \, dx\\
&= \int_{0}^{1}p(x)r(x) \, dx + \int_{0}^{1}q(x)r9x \, dx\\
&= \innp{p(x),r(x)} + \innp{q(x), r(x)}
\end{align*}$$
- Commutativty is trivial.