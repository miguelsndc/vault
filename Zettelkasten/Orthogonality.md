---
tags: spaces, vector, linear-transformations
aliases: orthogonal, perpendicular
---
Let $V$ be a [[Vector Space]] with [[Inner Product|inner product]] $\innp{,}$. Two [[Vector|vectors]] $v,w \in V$ are said to be *orthogonal* (with respect to the stablished inner product), if $\innp{v, w}= 0$. if $v$ and $w$ are indeed orthogonal to each other, we write $v \perp w$.
## Properties
- $\vec{0} \perp v \;\;  \forall v \in V$; proof:
  $\innp{\vec{0}, v} = \innp{0 \cdot v, v} = 0  \cdot \innp{v, v} = 0$, therefore $\vec{0} \perp v$.
- $v \perp w \implies w \perp v$; proof:
  $v \perp w \implies \innp{v,w}= 0 = \innp{w, v} \implies w \perp v$. 
- If $v \perp w$ for all $w \in V$, then $v = \vec{0}$, proof:
  Note that if $v \perp w \; \forall w \in V$, let $w = v$, then $v \perp v$, which is only possible if $v = \vec{0}$.
- If $v_{1} \perp w$ and $v_{2}\perp w$ then $v_{1}+ v_{2}\perp w$; proof:
  $v_{1} \perp w \implies \innp{v_{1}, w} = 0$
  $v_{2}\perp w \implies \innp{v_{2},w}=0$
  So $\innp{v_{1}, w} + \innp{v_{2}, w}= 0 \implies \innp{v_{1}+ v_{2},w}= 0 \implies v_{1}+v_{2}\perp w$.