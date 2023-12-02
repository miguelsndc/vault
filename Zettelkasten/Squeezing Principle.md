---
tags: limits
---
Let us show the **Squeezing Principle for [[Epsilon-Delta Definition of a Limit|limits]]**: Suppose that $f(x) \le g(x) \le h(x)$ for all $x \ne p$ in some neighborhood $N(p)$, suppose also that:
$$
\lim_{x\to p}f(x) =\lim_{x\to p}h(x)=a
$$
Then we also have  $\lim_{x\to p}g(x)=a$.

The idea behind this is that if $f \le g \le h$ then $0 \le g-f \le h-f$ by subtracting $f$ from all members. if we let $G(x) = g-f$ and $H(x)=h-f$ we have:
$$\begin{align*}
0&\le G(x) \le H(x)
\end{align*}
$$
In the case $H(x)\to 0$ as $x \to p$, if we let $N_{1}(0)$ be the neighborhood around $0$, since  $H(x)\to 0$ as $x \to p$ it follows that there is some neighborhood $N_{2}(p)$ such that $H(x) \in N_{1}(0)$ whenever $x \in N_{2}(p)$ and $x\ne p$.

Then the [[Inequality]] $0 \le G \le H$, states that $G(x)$ is no further from $0$ than $H(x)$ if $x \in N_{2}(p)$, Therefore $G(x) \in N_{1}(0)$ for such $x$ and hence $G(x) \to 0$ as $x \to p$;

> Roughly we say that if the distance of $g$ from $f$ $g-f$ is less than or equal to the distance of $h$ from $f$,  $h-f$, since $h \to 0$, we also have $g \to 0$ since $g$ is no further away from $0$ as $h$ is. 

