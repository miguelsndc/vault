---
tags: matrix
aliases: elementary, elementary matrix
---
Elementary [[Matrix Definition|matrix]] is a [[Identity Matrix]] with exactly one [[Basic Row Operations in Matrices|basic operation]] applied, it's useful when [[Matrix Multiplication|multiplying]] by a arbitrary matrix to eliminate some member, See:
Let $A=\begin{pmatrix}1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{pmatrix}$, What matrix we need to multiply this by to eliminate $A_{21}=3$?
## Workflow 
Notice that to eliminate $3$ in row $2$ we need to multiply row $1$ by $-3$ and add back to row $2$, which matrix can accomplish this ? Each column in the matrix far left will multiply each row in matrix far right, So our requirements is:

- We don't want to mess in row $1$ 
- We don't want to mess in row $2$
- We want to multiply row $1$ by $-3$ and add to row $2$.

Our first row will be: $\begin{pmatrix}1&0&0\end{pmatrix}$, we leave row $1$ as it is by putting $1$ in column $1$, and since we don't want to add anything to it, we put zeros in the other columns.

Our third row will be $\begin{pmatrix}0&0&1\end{pmatrix}$, since we don't change row $3$ by zeros everywhere that is not column $3$, where we add $1$.

Our second column is the trick, it has to multiply row $1$ by $-3$ and add to row $2$, since columns in multiplication get combined with rows in a [[Dot Product|dot product]] kind of way, can do row $2$ like: $\begin{pmatrix}-3&1&0\end{pmatrix}$, since we are multiplying row $1$ by $-3$ and adding to row $2$ that is just there, the resulting dot product will be the new row $2$, so our operation looks like:
$$\begin{align*}
\begin{pmatrix}
1 & 0 & 0\\
-3 & 1 & 0\\
0 & 0 & 1\\
\end{pmatrix}
\cdot
\begin{pmatrix}
1 & 2 & 1\\
3 & 8 & 1\\
0 & 4 & 1\\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 & 1\\
0 & 2 & -2\\
0 & 4 & 1\\
\end{pmatrix}
\end{align*}$$
Notice how the left matrix is a form of [[Identity Matrix]], called the [[Elementary Matrix]], by adding one [[Basic Row Operations in Matrices|basic operation]] on it and multiplying by $A$ we got a new matrix with a brand new [[Pivot]] in column $1$.

