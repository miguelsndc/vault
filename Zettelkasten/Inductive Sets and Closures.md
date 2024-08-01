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
- $Y$ is closed under the functions of $F$, that is: If $w_{1},w_{2},\cdots, w_{n} \in Y, f\in F$ 