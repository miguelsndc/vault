---
tags: matrix, systems
---
[[A = LU Factorization]] regarding the [[Non-Singular Case Matrix of a System]], is different, since non-singular matrices require row [[Row Exchanges|exchanges]], with row exchanges we cannot *form a [[Lower Triangular Matrix]] with non-zero diagonals*, so **LU** is done, notice that $U$ is fine.
However, by perfoming the row exchanges all at once in matrix $PA$ where $P$ is the product of all the [[Permutation Matrix|permutation matrices]], with $PA$ we can find a $LU$ or [[LDU Factorization]].

> *In the non-singular case, there is a permutation matrix $P$ that reorders the rows of $A$ such that $PA$ admits a factorization with nonzero [[Pivot|pivots]]: $PA= LU$ or $PA = LDU$, **in this case, there is one solution to $Ax = b$** and it is found by elimination with row exchanges, in the singular case, no reordering can avoid a zero pivot.*



