---
tags: logic
---
Let $PROP$ be the [[Sets|set]] of valid expressions of #propositional-logic , we want to prove that $PROP$ is a [[Freely Generated Sets|freely generated set]], thus we have to show each property:

Let $X$ be the [[Theorems and Proofs for Basis and Dimension|basis]], and $F = \{ f_{\lor}, f_{\land}, f_{\implies}, f_{\lnot} \}$. Thus $PROP$ is the [[Inductive Sets and Closures|inductive closure]] of $X$ over $F$, so we want to check if $PROP$ fulfills the three requirements:
- The functions $f_{\lor}, f_{\land}, f_{\implies}, f_{\lnot}$ are [[Injective Functions|injective]], because when applied to distinct elements, they yield different results.
- There is no two functions in $F$ whose [[Range]]s aren't [[Disjoint Set|disjoint]].
- No element of $X$ belongs to the [[Range in Discrete Math|range]] of some function of $F$.
Thus $PROP$ is freely generated.