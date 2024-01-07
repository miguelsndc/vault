---
tags: matrix, systems
aliases: singular
---
If [[Gaussian Elimination]] worked well in $k - 1$ columns but creates a $0$ [[Pivot|pivot]] in column $k$, if the elements **below** the pivot *in* column $k$ are non-zero, in row $l$, for example, [[Row Exchanges|exchange]] row $k$ and row $l$, and this allows elimination to proceed.

If the column below the pivot is all zeros, there is no exchange that can be done, this means the matrix is ***singular***. 
We found pivots $k$ through $n$ in $k$ through $n$ [[Equation|equations]], if there's a $0$ pivot the this unknown is not to be found, we have *less unknowns than equations*, this means that the [[Definition of a System of Linear Equations|system]] either has **infinetly many** solutions or **no solution at all**.****
