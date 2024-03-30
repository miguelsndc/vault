---
tags: spaces, vector
aliases: fourier coefficient
---
Let $V$ be a [[Vector Space]] with [[Inner Product|inner product]] $\innp{,}$, and let $\beta = \{v_{1},v_{2},\cdots, v_{n}\}$ be a [[Orthogonal Basis]] of $V$, and also let $w \in V$.
Then $w$ can be written as [[Linear Combinations|linear combination]] of $\beta$:
$$\begin{align*}
w &= x_{1}v_{1}+x_{2}v_{2}+\cdots+x_{n}v_{n}
\end{align*}$$
Take the inner product with respect to a arbitrary $v_{i}$ [[Vector]]:
$$\begin{align*}
\innp{w,v_{i}}&= \innp{v_{i}, x_{1}v_{1}+x_{2}v_{2}+\cdots+x_{n}v_{n}}\\
\innp{w,v_{i}}&=  x_{1}\innp{v_{i},v_{1}}+ \cdots+ x_{i}\innp{v_{i},v_{i}}+\cdots+x_{n}\innp{v_{i},v_{n}}\\
\innp{w,v_{i}}&= x_{i}\innp{v_{i}, v_{i}}\\
\therefore x_{i}&= \frac{\innp{w, v_{i}}}{\innp{v_{i},v_{i}}}
\end{align*}$$
The $i$-th [[Vector Coordinates|coordinate]] of $w$ is  