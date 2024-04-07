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
This can also be done using just matrices, since the projection is merely a [[Linear Transformations|transformation]], it can be expressed with matrices. This [[Matrix Definition|matrix]] is: $\frac{u\cdot u^{T}}{u^{T}u}$. The numerator will be a matrix and the denominator a scalar. Note that $u$ is a [[Vector Matrix Form|column vector]] and $u^{T}$ is a [[Vector Matrix Form|row vector]]. This will give a matrix $P$ such that $\proj{v}{u}=Pv$.