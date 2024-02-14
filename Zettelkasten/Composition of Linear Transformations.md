---
tags: linear-transformations
---
Consider two [[Linear Transformations]] $T:V \rightarrow W$ and $S:W\rightarrow U$, the *composition of $S$ with $T$*, $S\circ T$, is defined as $S \circ T : V \rightarrow U$, $S(T(v)), v \in V$. The concept works similarly to [[Composite Functions]].

> Proposition: Let $S$ and $T$ be linear transformations, then $S\circ T$ is a [[Linear Transformations|linear transformation]]. 

1. $S\circ T (u+v) = S\circ T(u) + S \circ T(v) \implies S(T(u+v))= S(T(u) + T(v))$, since $T$ is a linear transformation. $S(T(u) + T(v)) = S(T(u)) + S(T(v))$, since $S$ is a linear transformation, hence $S\circ T(u+v) = S\circ T(u) + S\circ T(v)$.
2. $S\circ T(ku) = k\cdot S\circ T(u)$. $S\circ T(ku)$