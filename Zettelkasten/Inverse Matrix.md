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

However there is a convenient method for $3 \times 3$ or maybe even $4 \times 4$ matrices, there are better algorithms for bigger matrices. Using cofactor expansion and minor matrices, the formula is:
$$\begin{align*}
\frac{1}{\det(A)}\cdot \f{Adj}(A)=A^{-1}
\end{align*}$$
Where $\f{Adj}(A)$ is the [[Adjoint Matrix]] of $A$. this comes from the fact that $A\cdot\f{Adj}(A)=\det(A)\cdot I$, a property of adjoint matrices.

The steps are, given a given matrix $A$:
- Find the [[Minor Matrix]] of $A$:
	- The minor is a matrix $M$ where each $M_{ij}$ entry is computed by calculating the determinant of the $2\times 2$ [[Submatrix]] of $A$ when we "delete" the $i$-th row and $j$-th column from $A$.
- Flip the signs of $M$ according to the cofactor matrix:
	- Modify $A$ according to the formula: $M_{ij} \leftarrow (-1)^{i+j}\cdot M_{ij}$
-  Now we [[Transposes|transpose]] the modified $M$ matrix and we have the adjoint.
- Then we just divide by the determinant of $A$, not the determinant of $M$.

> It's worth noticing that matrices with [[Determinant in 2 dimensions|determinant]] equal to zero have no inverse, so it might be better to first calculate the determinant and only procceed if it's non-zero.

