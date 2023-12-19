---
tags: matrix
---
Let $A$ be a $m\times n$ [[Matrix Definition|matrix]] and $x$ be a $n \times 1$ [[Vector Matrix Form|column vector]], we shall obtain the product $Ax = b$.
 
There's two ways to approach this multiplication, one that goes through every column of every row of $A$ and another that provides a combinations of the columns of $A$, we shall discuss each one separately:
# First Approach
The product of a row and a column is a number called the [[Scalar Product|dot product]], multiplying a matrix times a column will produce a **column vector** with dimensions $1\times n$ where $n$ is the number of rows in the matrix. 
Aware of this behavior, we shall compute the product between the $i$th row of $A$ and $x$, to produce the $j$th row of $b$, this will hold for all rows of $b$.

>See that this only works if the number of columns of $a$ equals the number of rows in $x$.


$$\begin{align*}
A_{i}&= \begin{pmatrix}a_{1} & a_{2}&\cdots &a_{n}\end{pmatrix}\\
x&= \begin{pmatrix}x_{1}\\
x_{2}\\
\vdots\\
x_{n}\end{pmatrix}\\
b_{j}&= (a_1x_1+a_2x_2+\cdots+a_{n}x_{n})
\end{align*}$$
Since a row times a column produces a single number, $b$ will have as much rows as $A$ and as much columns as $x$.
# Second Approach
The product can be computed by multiplying every column of $A$ by its corresponding $x$ entry. Like:
$$\begin{align*}
A&= \begin{pmatrix}2 & 3\\
4 & 0\end{pmatrix},\; x=\begin{pmatrix}1\\5\\\end{pmatrix}\\
Ax&= \begin{pmatrix}2\\4\end{pmatrix}(1)+\begin{pmatrix}3\\0\end{pmatrix}(5)\\
&= \begin{pmatrix}2\\4\end{pmatrix}+\begin{pmatrix}15\\0\end{pmatrix}\\
&= \begin{pmatrix}17\\4\end{pmatrix}
\end{align*}$$
Note