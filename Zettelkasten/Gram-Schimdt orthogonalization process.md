---
tags: spaces, vectors
aliases: gram-schmidt
---
Let $\beta = \{v_{1}, v_{2}, \cdots, v_{n}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] for a [[Vector Space|vector space]] $V$ equipped with [[Inner Product|inner product]] $\innp{,}$. It's possible to obtain a [[Orthonormal Basis|orthonormal]] from $\beta$ using the *gram-schmidt orthogonalization process*. This works for any space.
The key idea is to choose a initial [[Vector|vector]] $v_{1}'$, then figure out a vector $v_{2}'$  from $v_{2}$ that is orthogonal to $v_{1}'$, then a $v_{3}'$ that is orthogonal to both $v_{1}'$ and $v_{2}'$, and so on until the $n$-th vector.
# Process
Let $v_{1}' = v_{1}$. We need to find, from $v_{2}$, a vector $v_{2}'$ that is [[Orthogonality|orthogonal]] to $v_{1}'$, that is, $\innp{v_{2}', v_{1}'}=0$. Let $v_{2}' = v_{2} - cv_{1}'$. where $$ 