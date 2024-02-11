---
tags: linear-transformations
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
Consider $\nu(T) = \{\vec{0}\}
