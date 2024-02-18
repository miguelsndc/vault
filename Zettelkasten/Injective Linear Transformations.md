---
tags: linear-transformations
aliases: injective
---
[[Linear Transformations]] are special [[Functions]] that preserve addition and [[Multiplication by Scalar|scalar multiplication]] after application on [[Vector Space|vector spaces]], and as a function, transformations also share common properties with functions, such as being [[Injective Functions|injective]] (or one-to-one) functions.
Let $T: V \rightarrow W$ be a [[Linear Transformations|linear transformation]] and $V$ and $W$ vector spaces. $T$ is *injective* if $T(u) = T(v) \implies u = v$ for all $u,v \in V$, the [[Domain]].

> Theorem: $T: V \rightarrow W$ linear transformation is injective [[If and Only if]] the [[Kernel of a linear transformation|kernel]] $\nu(T) = \vec{0}$ and the [[Theorems and Proofs for Basis and Dimension|dimension]] $\dim[\nu(T)]= 0$.
## Proof
Going: 
Assume $T:V \rightarrow W$ is injective, we want to prove that $\nu(T) = \vec{0}$.
Consider $\nu(T)$; $u \in \nu(T) \implies u = \vec{0}$, $T(\vec{0}) = \vec{0}$
$T(u) = T(v) \implies u = \vec{0}$ (since $T$ is one to one).
$\implies \nu(T) = \{\vec{0}\}$.
Coming: 
Consider $\nu(T) = \{\vec{0}\}$, we want to prove that $T$ is injective.
Let $u,v \in V \mid T(u) = T(v)$.
$T(u) - T(v) = \vec{0}$
$T(u-v) = \vec{0}$, Therefore $u - v \in \nu(T)$.
Como $\nu(T) = \{\vec{0}\} \implies u - v = \vec{0} \implies u = v$.
___
## How to know if it is
Since $\nu(T) = \vec{0}$, then the [[Homogeneous System]] defining the [[Kernel of a linear transformation|kernel]] of $T$ *must* have a unique solution, this means, all [[Vector|vectors]] must be [[Linear (In)dependence.|linearly independent]]. Therefore build the system and put it in [[Row Reduced Echelon Form]].
$\rm{Example}:$ 
Let $T: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ defined by $T(x,y,z)=(x+y-z,x-y+z,-x+2y)$, determine wheter $T$ is injective or not.
$\nu(T) = \{(x,y,z) \in \mathbb{R}^{3} \mid T(x,y,z) = (0,0,0) \}$. Therefore:
$$\begin{align*}
\nu(T)&= \begin{cases}
x+y-z&= 0\\
x-y+z&= 0 \\
-x+2y&= 0 
\end{cases}
\end{align*}$$
Checking [[Linear (In)dependence.|dependence]]:
$$\begin{align*}
\begin{pmatrix}
1 & 1 & -1\\
1 & -1 & 1\\
-1 & 2 & 0
\end{pmatrix}\implies
\begin{pmatrix}
1 & 0 & 0\\
1 & -1 & 1\\
0 & 2 & 0
\end{pmatrix}\implies
\begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
\end{align*}$$
Therefore $\nu(T) = \{\vec{0}\} \therefore T$ is injective.
___
From the [[Kernel-Image Theorem]], specifically the case where $\dim(V) \gt \dim(W)$ for a [[Linear Transformations|transformation]] $T:V\rightarrow W$. Since: $\dim[\nu(T)] + \dim[\im(T)] = \dim(V)$, then:
$$\begin{align*}
\dim[\nu(T)]&= \dim(V) - \dim[\im(T)]
\end{align*}$$
But $\dim(V) \gt \dim[\im(T)]$, therefore $\dim(\nu(T)) \gt 0$ and therefore $T$ can't be injective.

> $T$ is injective if and only if the [[Theorems and Proofs for Basis and Dimension|dimension]] of the [[Domain]] is less or equal the dimension of the [[Range]].