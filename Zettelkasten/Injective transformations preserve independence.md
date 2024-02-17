---
tags: linear-transformation
---
Let $\alpha = \{v_{1},v_{2}, \cdots, v_{n}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] and $T:V \rightarrow W$ be a [[Injective Functions|injective]] [[Linear Transformations|transformation]], then, $\{T(v_{1}), T(v_{2}), \cdots, T(v_{n})\}$ is also independent.
## Proof
Suppose we have $a_{1}, a_{2},\cdots, a_{n}$ such that $$\begin{align*}
T(a_{1}v_{1}+a_{2}v_{2}+\cdots+a_{n}v_{n})&= T(\vec{0})\\
a_{1}Tv_{1}+a_{2}Tv_{2}+\cdots+a_{n}Tv_{n}&= \vec{0}
\end{align*}$$
Since $T$ is injective, $T\vec{0} = \vec{0}$ and we have $a_{1}v_{1}+a_{2}v_{2}+\cdots+a_{n}v_{n}= \vec{0}$. Since $\{v_{1},v_{2},\cdots,v_{n}\}$ is [[Linear (In)dependence.|independent]], $a_{1}=a_{2}=\cdots=a_{n}=0$ and so $\{Tv_{1},Tv_{2},\cdots,Tv_{n}\}$ is also independent.