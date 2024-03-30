---
tags: vector, spaces
---
With the notion of [[Inner Product]] and [[Fourier Coefficients]], one can *project* one [[Vector|vector]] $v$ into another vector $w$. such that, after the proccess, $v$ becomes a multiple of $w$, and $\innp{v - \proj{v}{w}, w} = 0$. We'll derive using $\R^{2}$, however, this applies to any $n$-dimensional space.

![[orthogonal_projection.excalidraw]]
From this let's derive the formula, we must discover $k$:
$$\begin{align*}
\innp{(u- k\cdot v), v}&= 0\\
\innp{u,v} - k\cdot \innp{v, v}&= 0\\
k&= \frac{\innp{u,v}}{\innp{v,v}}\\
\end{align*}$$
Therefore, $\proj{v}{w}=k \cdot v= \frac{\innp{u,v}}{\innp{v,v}}v$ 