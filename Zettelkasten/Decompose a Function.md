---
tags:
  - functions
  - transformations
date: 2023-10-09
"
page: 215
aliases:
  - decomposing
  - decompose
  - spread
---
We often build complicated [[Functions]] from simpler ones by [[Composite Functions|composition]], but we can also do the opposite, **build simpler functions from messy ones**. See:
$$\begin{align*}
F(x) &= \sqrt{x-3}
\end{align*}$$
We can split this function into a composite one by splitting into two arbitrary functions, let's say $g$ and $h$:
$$\begin{align*}
F(x) &= \sqrt{x-3}\\
h(x) &= x-3\\
g(x)&= \sqrt{x}\\
F(x) &= g(h(x))=(g\circ h)(x)=\sqrt{x-3}
\end{align*}$$