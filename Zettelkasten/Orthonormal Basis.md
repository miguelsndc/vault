---
tags: spaces, vector
aliases: orthonormal basis, orthonormal
---
Let $V$ be a [[Vector Space|vector space]] with [[Inner Product|inner product]] $\innp{,}$. A [[Theorems and Proofs for Basis and Dimension|basis]] $\beta = {v_{1},v_{2},\cdots, v_{n}}$ is callled **orthonormal** if it's [[Orthogonality|orthogonal]] and it's [[Vector|vectors]] are unitary, that is:
$$\begin{align*}
\begin{cases}
\innp{v_{i},v_{j}}&= 0 \;\; i\ne j\\
\innp{v_{i}, v_{i}}&= \norm{v_{i}}^{2}= \norm{v_{i}}= 1
\end{cases}\\
\end{align*}$$
This has some cool consequences, for example, notice that for a orthonormal basis the [[Fourier Coefficients]] of a given vector $w \in V$ are:
$$\begin{align*}
w &= x_{1}v_{1}+ \cdots x_{n}v_{n}\\
\vdots\\
x_{i}&= \frac{\innp{w, v_{i}}}{\innp{v_{i}, v_{i}}}
\end{align*}$$
But since $\innp{v_{i},v_{i}}= 1$, $x_{i}= \innp{w, v_{i}}$. Which makes operations much much simpler.
