---
tags: matrix
aliases: elementary, elementary matrix
---
Elementary [[Matrix Definition|matrix]] is a [[Identity Matrix]] with exactly one [[Basic Row Operations in Matrices|basic operation]] applied, it's useful when [[Matrix Multiplication|multiplying]] by a arbitrary matrix to eliminate some member, See:
Let $A=\begin{pmatrix}1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{pmatrix}$, What matrix we need to multiply this by to eliminate $A_{21}=3$?
## Workflow 
Notice that to eliminate $3$ in row $2$ we need to multiply row $1$ by $-3$ and add back to row $2$, which matrix can accomplish this ? Recall the concepts from [[Why is matrix multiplication not commutative]] and [[Scalar Product|dot product]], each column in the matrix far left will multiply each row in matrix far right, So our requirements is:
- We don't want to mess in row $1$ 
- We don't want to mess in row $2$
- We want to multiply row $1$ by $-3$ and add to row $2$.
- 