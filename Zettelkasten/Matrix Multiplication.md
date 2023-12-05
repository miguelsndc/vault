---
tags: matrix
aliases: multiplication, matrix multiplication, multiply, multiplying
---
>[!danger] Remember
>Matrix multiplication is **not** commutative. See [[Why is matrix multiplication not commutative]].

A [[Matrix Definition|matrix]] multiplied on the right by some [[Vector Matrix Form|column vector]] is the combination of the column of the matrix and the rows of the vector, see:
$$
\begin{bmatrix}a&b&c \\ d&e&f \\ g&h&i\end{bmatrix}
\cdot
\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix}
= 
\begin{bmatrix}3(a,d,g) \\ 4(b,e,h) \\ 5(c,f,i)\end{bmatrix}
$$
The multiplication of a matrix by a column vector is the multiplication of each **row** of the vector by each **column** of the matrix, resulting in a new column vector.

Same goes for **row vectors** on t, each column of the row vector is multipled 