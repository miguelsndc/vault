---
tags: vector
---
Let us prove $\abs{\innp{v,w}} \le \norm{v} \cdot \norm{w}$:
For all $t \in \R$ we have:
$$\begin{align*}
\innp{tv+w,tv+w} &\ge 0\\
\innp{v,v}t^{2} + 2\innp{v,w}t + \innp{w,w}&\ge 0
\end{align*}$$
$\Delta$ must be negative: $\Delta = 4\innp{v,w}^{2}- 4\innp{v,v}\innp{w,w}\le0$
That means:
$$\begin{align*}
4\innp{v,w}^{2}-4\norm{v} \cdot \norm{w}&\le 0\\
\abs{\innp{v,w}} &\le \norm{v} \cdot \norm{w}
\end{align*}$$
