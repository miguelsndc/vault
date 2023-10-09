---
tags:
  - functions
date: 2023-10-09
source: "[[James Stewart Precalculus.pdf]]"
page: 210
aliases:
  - function algebra
  - sum
  - diff
  - quotient
  - product
---
We can perform the basic operations with [[Functions]] just like [[Real Numbers]], *sum, difference, product and quotient*. We define the sum of $f + g$ like:
$$\begin{align*}
(f+g)(x)&= f(x)+g(x)
\end{align*}$$
The sum on the right-hand side only makes sense if $f$ and $g$ are defined, that means, if $x$ belongs to the [[Domain]] of both $f$ and $g$. In this case, if the domain of $f$ is $A$ and of $g$ is $B$, the domain of $f+g$ is $A \cap B$, same goes for **sum and difference**, **quotient** too, but we need to be careful to not divide by zero. 

###### Definition
For two functions $f$ with domain $A$ and $g$ of domain $B$ we can:
- **Sum**: $(f+g)(x) = f(x)+g(x)$ where domain is $A \cap B$
- **Difference**: $(f-g)(x) = f(x)-g(x)$ where domain is $A \cap B$
- **Product**: $(fg)(x) = f(x)g(x)$  where domain is $A \cap B$
- **Quotient**: $\left(\frac{f}{g}\right)(x) = \frac{f(x)}{g(x)}$ where domain is $\{x\in A\cap B \mid g(x) \ne 0\}$     