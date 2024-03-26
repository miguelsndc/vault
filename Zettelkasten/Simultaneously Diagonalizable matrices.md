---
tags: matrix, linear-transformations, eigen-everything
---
Given two [[Linear maps]] $T_{1}$ and $T_{2}$, both [[Diagonalizable Matrices|diagonalizable]], this means that there exists two [[Theorems and Proofs for Basis and Dimension|basis]] $\alpha_{1}$ and $\alpha_{2}$, where $T_{1\alpha_{1}}^{\alpha_{1}}$ and $T_{2\alpha_{2}}^{\alpha_{2}}$ are [[Diagonal Matrix|diagonal]].
However, we can't guarantee that $\alpha_{1}= \alpha_{2}$.
Such relationship between two maps where both admit the same [[Sets|set]] of [[Linear (In)dependence.|linearly independent]] [[Eigenvalues and Eigenvectors|eigenvectors]] as [[Theorems and Proofs for Basis and Dimension|basis]], only *exist if $T_{1}$ and $T_{2}$ commute.* That is, $T_{1}\circ T_{2} = T_{2} \circ T_{1}$.
On practice, let $\beta$ be a basis of $V$, and, verified that $T_{1}$ and $T_{2}$ are diagonalizable, if, also $[T_{1}]^{\beta}_{\beta}[T_{2}]^{\beta}_{\beta} = [T_{2}]^{\beta}_{\beta}[T_{1}]^{\beta}_{\beta}$, then, we can conclude that $T_{1}$ and $T_{2}$ are simultaneaously diagonalizable.