---
tags:
  - sets
aliases:
  - subset
date: 2023-11-06
---
A [[S1/MD/Sets|set]] $A$ is a subset of $B$ **if and only if** every element in $A$ is also in $B$.
$A \subseteq B$ means *A subset of B*. See:
$$\begin{align*}
\forall x (x\in A \implies x \in B)
\end{align*}$$
Look at the [[Venn Diagram]]:
![[Subset.excalidraw]] 
We can clearly see that $A$ **is contained** within $B$, which is another way of saying the same shit.
___
For every set $S$, $\emptyset  \subseteq S$ and $S \subseteq S$. See, by the definition of subsets:
$$\begin{align*}
\forall x(x \in \emptyset \implies x \in S)\\
\forall x(F \implies S)
\end{align*}$$
We know that if the left side of a [[Implication]] is **false**, then the whole implication is true, no matter the value of the right side.
See:
$$\begin{align*}
\forall x (x\in S \implies x \in S)
\end{align*}$$
When both sides are equal, the implication will be true.
So we verified both propositions.