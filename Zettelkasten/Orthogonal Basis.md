---
tags: spaces
---
Let $\{v_{1},v_{2},\cdots, v_{n}\}$ be a [[Sets|set]] of non-zero [[Vector|vectors]], where every pair $(v_{i},v_{j})$ with $i \ne j$ is [[Orthogonality|orthogonal]], that is: $\innp{v_{i}, v_{j}} = 0 \;\; i\ne j$, is [[Linear (In)dependence.|linearly independent]].
# Proof
Let $a_{1}v_{1}+a_{2}v_{2}+ \cdots + a_{n}v_{n}= 0$
Taking the [[Inner Product]] of each $\innp{a_{i}v_{i}, v_{j}}$:
$$\begin{align*}
a_{1}v_{1} + a_{2}v_{2}+ \cdots + a_{n}v_{n}&= 0\\
\innp{a_{1}v_{1} + a_{2}v_{2}+ \cdots + a_{n}v_{n}, v_{i}}&= \innp{0, v_{i}}\\
a_{1}\innp{v_{1},v_{i}} + \cdots + a_{i}\innp{v_{i},v_{i}}+ \cdots+ a_{n}\innp{v_{n}, v_{i}}&= 0\\
\end{align*}$$
Since they're all orthogonal to each other, every $\innp{v_{i},v_{j}}$ equals $0$, which leaves us with $a_{i}\innp{v_{i}, v_{i}}= 0$, since $\innp{v_{i},v_{i}} \gt 0$ since $v_{i}\ne \vec{0}$, this implies that $a_{i}$ must be $0$. this is valid for all $i=1,2,3,\cdots,n$, are therefore $\{v_{1},v_{2}, \cdots, v_{n}\}$ is [[Linear (In)dependence.|linearly independent]].
___
Follows from the previous theorem that $\{v_{1},v_{2},\cdots, v_{n}\}$ is a [[Theorems and Proofs for Basis and Dimension|basis]] for the $n$-dimensional space, and is called *(no shit)* an **orthogonal basis**.