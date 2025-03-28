---
tags: spaces
---
Consider $V$ a [[Vector Space]] and $S_{1},S_{2} \subset V$ where $S_{1}$ and $S_{2}$ are [[Linear Subspaces|subspaces]], then, $S_{1} \cap S_{2}$ is also a subspace. Consider the definition:
$$\begin{align*}
S_{1}\cap S_{2}=\{v\in V \mid v \in S_{1}\text{ and } v \in S_{2}\}
\end{align*}$$
Proof:
1. Since $S_{1}$ and $S_{2}$ are both subspaces of $V$ they both contain $\vec{0}$, so $\vec{0} \in S_{1}\cap S_{2}$.
2. Let $u,v \in S_{1}\cap S_{2}$, then, in particular $u,v \in S_1$, since $S_1$ is a subspace so $u+v \in S_{1}$, same holds for $S_{2}$. so $u+v \in S_{1}\cap S_{2}$.
3. Let $a$ be a [[Scalar]], so if $u \in S_1$ then $au\in S_1$, same holds for $S_{2}$, so $au \in S_{1}\cap S_{2}$.
Now consider two subspaces in their [[Homogeneous System]] representation:
$$\begin{align*}
S_{1}=\Bigg\{ (x,y,z,w) \in \mathbb{R}^{4} \mid \begin{cases}
x+y+z+w=0\\
2x-y+3z=0\\
\end{cases}\Bigg\}\\\\
S_{2}=\Bigg\{ (x,y,z,w) \in \mathbb{R}^{4} \mid \begin{cases}
x+2w=0\\
2x+3y=0\\
\end{cases}\Bigg\}
\end{align*}
$$
Hence the intersection $S_{1}\cap S_{2}$ is found by trivially joining the systems together.

$$\begin{align*}
S_{1} \cap S_{2}=\Bigg\{ (x,y,z,w) \in \mathbb{R}^{4} \mid \begin{cases}
x+y+z+w=0\\
2x-y+3z=0\\
x+2w=0\\
2x+3y=0\\
\end{cases}\Bigg\}\\\\
\end{align*}$$
We can turn this into a [[Augmented Matrix]] and find the [[Echelon Form|echelon]] form to gain more information about the [[Linear Subspaces|subspace]], whether it has some free variables or whatever, but it's pretty much trivial shit to do.
____
Let $E$ be a [[Vector Space]], and let $L$ be a [[Sets|set]] of indices, i claim that for $\lambda \in L$, $F_{\lambda}$ is a [[Linear Subspaces|subspace]]. Therefore:
$$\begin{align*}
\bigcap_{\lambda\in F} F_{\lambda} 
\end{align*}$$
is also a subspace of $E$, it follows from the example given in [[Linear Subspaces|subspace]]s, that the set of vectors $v=(x_{1},x_{2},\cdots,x_{n})\in \R$ whose coordinates satisfy the $m$ equations below:

$$\begin{align*}\\
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = 0 \\
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = 0 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = 0
\end{cases}
\end{align*}$$
is a vector subspace of $R^{n}$, the intersection $F=F_{1}\cap\cdots\cap F_{n}$ of the [[Hyperplanes]] $F_{i}$ defined above.