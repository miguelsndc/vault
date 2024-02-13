---
tags: linear-transformations
aliases: kernel image theorem
---
Let $T:V \rightarrow W$ be a [[Linear Transformations|linear transformation]]. Then $\dim[\nu(T)] + \dim[\im(T)] = \dim(V)$, (the [[Domain]]), this relationship is closely related to the [[Rank-Nullity Theorem]].
## Proof
Let $T: V \rightarrow W$, Let $\{v_{1},v_{2}, \cdots, v_{r}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] of the [[Kernel of a linear transformation|kernel]] of $T$. Completing this basis with [[Linear (In)dependence.|linearly independent]] [[Vector|vectors]], $\{v_{1},v_{2},\cdots, v_{r},v_{r+1}, v_{r+2}, \cdots, v_{n}\} = \alpha$ (basis of $V$)
Since the vectors up to $v_{r}$ are a basis for the kernel, we want to prove that the vectors from $v_{r+1}$ up to $v_{n}$ are a basis for the [[Image of a linear transformation|image]] $\im(T)$.
Applying $T$ to $\alpha: = \{T(v_{1}), T(v_{2}), \cdots, T(v_{r}), T(v_{r+1}), \cdots, T(v_{n})\}$, this is a valid [[Span|spanning set]] for $\im(T)$. Since $\alpha$ spans $\im(T)$, we just need to prove they're [[Linear (In)dependence.|linearly independent]].
$$\begin{align*}
\vec{0} &=  a_{r+1}T(v_{r+1})+ a_{r+2}T(v_{r+2})+\cdots+a_{n}T(v_{n})
\end{align*}$$
Since $T$ is linear:
$$\begin{align*}
\vec{0} &= T(a_{r+1}v_{r+1}+ a_{r+2}v_{r+2}+\cdots+a_{n}v_{n}) 
\end{align*}$$
This vector $a_{r+1}v_{r+1}+ a_{r+2}v_{r+2}+\cdots+a_{n}v_{n}$, being zero after $T$ implies that it is in the kernel, so it can be written as a [[Linear Combinations|linear combination]] of the [[Theorems and Proofs for Basis and Dimension|basis]] of $\nu(T)$ we defined earlier:
$$\begin{align*}
a_{r+1}v_{r+1}+ a_{r+2}v_{r+2}+\cdots+a_{n}v_{n} &= a_{1}v_{1}+a_{2}v_{2}+\cdots a_{r}v_{r}\\
a_{1}v_{1}+a_{2}v_{2}+\cdots a_{r}v_{r}-a_{r+1}v_{r+1}- a_{r+2}v_{r+2}-\cdots-a_{n}v_{n} &= \vec{0}
\end{align*}$$
The vectors $v_{1},v_{2},\cdots, v_{r},v_{r+1}, v_{r+2}, \cdots, v_{n}$ form a basis for $V$