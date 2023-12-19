---
tags: matrix
aliases: multiplication, matrix multiplication, multiply, multiplying, product
---
If we are given any pair $E$ and $A$ of [[Matrix Definition|matrices]], to multiply them, first their *shape must allow it*. Multiplication of matrices is done through [[Scalar Product|dot product]], and one of the restrictions for the dot product operation is that the [[Vector|vectors]] **must be of the same dimension**.

If we aim to find $E \times A$ *(Notice E is multiplying on the left)*, the multiplication is done by taking the dot product of the row $i$ of $E$ with the column $j$ of $A$. See the rows of $E$ and the columns of $A$ as vectors of whatever the dimension they're in.

> **Notice that E is multiplying of the left**, if the product were $A\cdot E$. the opposite is applied.

Since the restriction of dot product is that the vectors must be of the same dimension, the numbers of columns of $E$ must match the number of rows in $A$.
Also notice that if we call the matrix $EA = x$, the product between the $i$th row of $E$ and the $j$th row of $A$ produces the entry $x_{ij}$.
Since $x$ will have as much rows as $E$ and as much columns as $A$, if $E_{m \times n}$ and $A_{n \times p}$, $x$ will be $m \times p$.