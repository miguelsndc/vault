---
tags: linear-transformations
aliases: maps, map, linear map
---
A *Linear map* $T$ is a [[Linear Transformations|transformation]] from a [[Vector Space|vector space]] $V$ into itself. $T:V \rightarrow V$, namely. There's some cool things to notice:
- The [[Matrix Definition|matrix]] of a linear map is *always square*.
  This is quite obvious since it maps $n$-dimensional [[Vector|vectors]] to $n$-dimensional vectors, however, [[Theorems and Proofs for Basis and Dimension|dimension]] is not the only factor that makes a linear transformation a map. $T: \mathbb{R}^{3} \rightarrow P_{2}$ maps three-dimensional spaces but it's not a map.
- A Linear map is [[Injective Linear Transformations|injective]] [[If and Only if|if and only if]] it's surjective.
  By the [[Kernel-Image Theorem]], $\dim(\nu(T)) + \dim(\im(T)) = \dim(V)$. Suppose $T$ is injective, then $\dim(\nu(T)) = 0$, therefore, $\dim(\im(T))= \dim(V)$. But $T$ maps $V$ to $V$, therefore $T$ is also [[Surjective Linear Transformations|surjective]]. Same goes the other way around.
- A Linear map isn't necessarily always inversible.
  The necessary conditions for a [[Linear Transformations|transformation]] to have an [[Inverse of a Linear Transformation|inverse]] is for it to be [[Bijective Linear Transformations|bijective]]. Even though a linear map $T:V \rightarrow V$ maps $V$ into itself, it's [[Image of a linear transformation|image]] might still be a [[Linear Subspaces|subspace]] of $V$. and it won't be neither injective nor surjective, hence not having an inverse.