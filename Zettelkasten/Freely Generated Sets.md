---
tags: logic
---
To prevent *ambiguity* between two expressions, we must ensure that every expression has exactly one way to be defined, to achieve this we use the mathematical concept of "Freely Generated [[Sets]]"

Let $A$ be a [[Sets|set]] and $X$ a [[Subsets|subset]] of $A$. Suppose that $F$ is a set of [[Functions|functions]] over $A$, each with it's own arity, ($F:A^{n}\rightarrow A$), the [[Inductive Sets and Closures|inductive closure]] $X_{+}$ over $F$ is a freely generated set if:
- The functions of $F$ are all [[Injective Functions|injective]] when the [[Domain]] is restricted to $X_{+}$
There can't be two ways to generated the same result
- Any two different functions of $F$ have a [[Disjoint Set|disjoint]] [[Range in Discrete Math|range]] over $X_{+}$
There can't be two ways to generate the same result for two different functions, if the [[Intersection]] isn't empty, that's not true
- No element from the [[Definitions of Logic|basis]] is on the [[Range in Discrete Math|range]] of one $f \in F$ over $X_{+}$
There will be two ways to generate the basis, one is the definition we declared and the other is the generated through the functions.

These properties ensure that expressions are generated without ambiguity and are uniquely formed. This allows the expressions to be broken down into atoms, allowing the evaluation of the final result.