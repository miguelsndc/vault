---
tags:
  - logic
---
The [[Definitions of Logic|alphabet]] $\Sigma = V \cup \{0,1,\land,\lor,\lnot,\implies,(,)\}$ where $V$ is the set of all variables $V=\{A,B,C,D,...\}$, Let $A = \Sigma^{*}$, the set of all possible expressions.
Let's define $\rm{EXPR} \subseteq \Sigma^{*}$, $\rm{EXPR}$ being the [[Definitions of Logic|language]] of #propositional-logic. Or, in other words, the set of legitimate expressions.

Let's define the set $F$, the set of all functions in propositional logic. That is:
- $f_{\lnot}:\Sigma^{*}\rightarrow \Sigma^{*}$ as $f_{\lnot}(w)=(\lnot w)$.
- $f_{\land}:\Sigma^{*} \times \Sigma^{*} \rightarrow \Sigma^{*}$ as $f_{\land}(w_{1},w_{2})=(w_{1}\land w_{2})$.
- $f_{\lor}: \Sigma^{*} \times \Sigma^{*} \rightarrow \Sigma^{*}$ as $f_{\lor}(w_{1}, w_{2})= (w_{1} \lor w_{2})$.
- $f_{\implies}:\Sigma^{*} \times \Sigma^{*} \rightarrow \Sigma^{*}$ as $f_{\implies}(w_{1},w_{2}) = (w_{1}\implies w_{2})$
Notice that $F$ is defined over $\Sigma^{*}$, so it certainly will produce non-legitimate expressions. 
___
## Inductive Sets

A given [[Subsets|subset]] $Y$ of $A$ is *inductive* over $X$ ([[Definitions of Logic|basis]]) and $F$ (*generator functions*) if:
- $Y$ contains $X$.
- $Y$ is closed under the functions of $F$, that is: If $w_{1},w_{2},\cdots, w_{n} \in Y, f\in F$ and the arity of $f=n \implies f(w_{1},w_{2},\cdots,w_{n}) \in Y$. In other words, arguments and results belong to the same set.

## Inductive Closures

A *closure* is the smallest set that preserves some property, in this case, the inductive closure of $X$ over $F$ is the smallest set that contains $X$ and is closed under the functions of $F$. (See the definition of inductive sets above).

The inductive closure can be constructed in two different ways. **Top-down** and **Bottom-up**.

**Top-down**
Let $I$ be the family of all inductive sets of $X$ over $F$. Then the following holds:
$$\begin{align*}
\bigcap_{i=0}^{\infty}I_{i}=X^{+}
\end{align*}$$
Where $X^{+}$ is the inductive closure. Mathematically, this is perfectly valid, however, **computationally speaking** we can't really list all inductive sets since there's infinitely many of them. So we use the bottom-up approach:

**Bottom-up** 
Let $X_{0}$ be the basis $X$, let $F$ be the family of generator functions over $X$, then we can do something like:
$$\begin{align*}
X_{1}&= X_{0}\cup
\end{align*}$$
