---
tags: functions
---
Let $f$ be [[Differentiability and Continuity|differentiable]] on some open [[Intervals|interval]] $I$. The [[Sets|set]] of points $x$ where $f'(x) = 0$ or $f'(x)$ is undefined are called the *critical points* of $f$.
Critical points represent change in the [[Increasing and Decreasing intervals|rate of change]] of a function, whether it's changing from [[Increasing and Decreasing intervals|increasing]] to [[Increasing and Decreasing intervals|decreasing]], or changing in [[Concavity]].
Examples are:
Let $g(x) = x^{3}-2x^{2}+x+2$. Find the intervals of growth and decay of $g$.
$$\begin{align*}
g'(x) =3x^{2}-4x+1\\
\end{align*}$$
Set $g'(x) = 0$ and solve for $x$, which gives $x'=1$ and $x'' = \frac{1}{3}$. Since:
$$\begin{align*}
\lim_{x\rightarrow -\infty} g'(x)&= \infty\\
\lim_{x\rightarrow +\infty} g'(x)&= \infty
\end{align*}$$
We see that:
$$\begin{align*}
\begin{cases}
g'(x) \gt 0 \;\forall x \in \left(-\infty, \frac{1}{3}\right)\cup(1, \infty)\\
g'(x) \lt 0
\end{cases}
\end{align*}$$
