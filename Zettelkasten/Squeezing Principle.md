---
tags: limits
---
Suppose that $f(x) \le g(x) \le h(x)$ for all $x \ne p$ in some neighborhood $N(p)$, suppose also that:
$$
\lim_{x\to p}f(x) =\lim_{x\to p}h(x)=a
$$
Then we also have $\lim_{x\to p}g(x)=a$.

The idea behind this is that if $f \le g \le h$ then $0 \le g-f \le h-f$, if we let $G(x) = g-f$ and $H(x)=h-f$ we have:
$$\begin{align*}
0&\le G(x) \le H(x)
\end{align*}
$$
Iif