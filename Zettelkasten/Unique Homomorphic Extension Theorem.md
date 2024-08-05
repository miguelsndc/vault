---
tags: logic
---
Let $A$ be a [[Sets|set]] and $X \subset A$. Suppose $F$ is a set of [[Functions]] over $A$, each with it's own arity. Let $B$ be another set, $G$ a set of functions over $B$ and $d$ a [[Bijective|bijection]] from $F$ to $G$ that preserves arity.

In this case, if $X_{+}$ is a [[Freely Generated Sets|freely generated set]], then for all functions $h: X \rightarrow B$, there exists a unique function $\hat{h}: X_{+}\rightarrow B$ such that:
- $\hat{h}(x)= h(x)$ for all $x \in X$;
- $\hat{h}(f(w_{1},\cdots, w_{n})) = g(\hat{h}(w_{1}),\cdots, \hat{h}(w_{n}))$ for all $f \in F$, arity $F = n$, $g = d(f)$ and $w_{1},\cdots,w_{n} \in X_{+}$.
Since there is only one way of breaking down $X_{+}$ into subexpressions all the way to the atoms, this theorem guarantees that there is only one function that effectively breaks it down, and then uses the *semantical* value of the atoms to build up the result. basically $\hat{h}$ is a helper function that traverses the syntax tree and once it reaches a leaf, it calls $h$ on the leaf and backtracks.