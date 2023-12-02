---
tags: limits
aliases:
- limit
- limits
---
Let $f$ be a [[Functions in Discrete Math|function]] and assume $A$ is a [[Real Numbers|real number]], and note that $f$ is a defined on some *neighborhood* of a point $p$. 

Note that we have two neighborhoods, $N_{1}(A)$, the neighborhood that tell us how close we want $f(x)$ to be to the limit $A$ in the $y$ axis, and $N_{2}(p)$, that tell us how close $x$ should be of $p$ so $f(x)$ is whithin the neighborhood $N_{1}(a)$.

>[!info] Intuitive Definition
>$f(x) \in N_{1}(a)$ whener $x\in N_{2}(p)$ and $x \ne p$

The essential part of the definition is, that for every $N_{1}(A)$, *there is* some $N_{2}(p)$ to satisfy it.

Let's call the distance of the neighborhoods from the limit $A$ and from the point $p$ as **radius**, the abrangence of the interval.

We can formulate the definition in terms of the radius of $N_{1}(A)$ and $N_{2}(p)$, it's conventional to name the radius of $N_{1}(A)$ as $\epsilon$, and the radius of $N_{2}(p)$ as $\delta$. The statement $f(x) \in N_{1}(A)$ is equivalent to the [[Inequality]]: $\mid f(x) - A \mid \lt \epsilon$, this means: *the [[Distance Between Skew Lines|distance]] of $f(x)$ from $A$ in will always lie in the interval $\epsilon$*. similarly, $x \in N_{2}(p) \land x \ne p$ is equivalent to $0 \lt \mid x - p \mid \delta$, which means: *the distance of $x$ from $p$ will always lie in the interval $\delta$, and will never be zero, since limits don't ever actually reach the point of approximation*.

So: let's rebuild:
>[!tip] Formal Definition of a Limit
>The symbol $lim_{x\to p}f(x) = A$ means that for every $\epsilon \gt 0$ there is a $\delta \gt 0$ such that $\mid f(x) - A \mid \lt \epsilon$ whenever $0 \lt \mid x - p \mid \lt \delta$. 

Where $\epsilon$ and $\delta$ are simply neighborhoods of $A$ and $p$.