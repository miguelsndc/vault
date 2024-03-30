---
tags: vector, spaces
---
With the notion of [[Inner Product]] and [[Fourier Coefficients]], one can *project* one [[Vector|vector]] $v$ into another vector $w$. such that, after the proccess, $v$ becomes a multiple of $w$, and $\innp{v - \proj{v}{w}, w} = 0$.
See:
![[orthogonal_projection.excalidraw]]
From this let's derive the formula:
$$\begin{align*}
\innp{(u- k\cdot v), v}&= 0\\
\innp{u,v} - k\cdot \innp{v, v}&= 0\\
k&= \frac{\innp{u,v}}{\innp{v,v}}\\
\end{align*}$$