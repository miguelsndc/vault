---
tags:
  - matrix
  - vector
aliases:
  - inverse
  - inverses
---
The inverse of a [[Matrix Definition|matrix]] $A$ is another matrix $M$ where $A \cdot M = I$. A matrix is *invertible* if and only if it's square, and if it is also a [[Bijective Linear Transformations|bijective]] [[Linear Transformations|transformation]], that is, the [[Image of a linear transformation|column space]] of $A$ has the same [[Theorems and Proofs for Basis and Dimension|dimension]] as the number of columns of $A$, and the [[Kernel of a linear transformation|null space]] of $A$ is just the zero vector.

The inverse can be found with the [[Row Reduced Echelon Form]] of a special matrix, the process is described here: [[Inverse of a Linear Transformation]], this method works for any $n \times n$ matrix.

However there is a convenient method for $3 \times 3$ or maybe even $4 \times 4$ matrices, using cofactor expas
