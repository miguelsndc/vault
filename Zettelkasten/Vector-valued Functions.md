---
tags: vector, functions
aliases: vector valued functions, vector function
---
A [[Vector]] valued [[Functions|function]] is a one-variable function $f:A \rightarrow \R^{n}$ $A \subset \R$ that maps every $t \in A$ in it's [[Domain]] to [[Vector|vectors]] in $\R^{n}$, every [[Components of vector along some direction|component]] of the vector is itself a function of $t$. specifically in $\R^{3}$, a vector function $\vec{r}(t)$ is given by:
$$\begin{align*}
\vec{r(t)}&= \hat{i}\,x(t) + \hat{j}\,y(t)+\hat{k}\,z(t)\\
&= \innp{x(t),y(t),z(t)}
\end{align*}$$
These being vectors that point from the origin to $r(t)$.
___
## Operations
Vector valued functions support both [[Vector|vector]] operations and [[Functions|function]] operations.

Let $F, G:A \rightarrow\R^{n}$ be two vector-valued functions, let $f:A\rightarrow \R$ be a [[Real Numbers|real]] function and $k \in \R$ a constant.

