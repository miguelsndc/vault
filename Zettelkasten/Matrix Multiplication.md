---
tags: matrix
aliases: multiplication, matrix multiplication, multiply, multiplying
---
>[!danger] Remember
>Matrix multiplication is **not** commutative.

To multiply two [[Matrix Definition|matrices]] where both **aren't** in [[Vector Matrix Form|column vector]] form nor [[Vector Matrix Form|row vector ]] form, we need to apply the [[Scalar Product|dot product]] between the rows of the one on **the left** and the **columns** of the one on the right.

Looks like:
![[Pasted image 20231205103418.png]]

- The number of **columns of the 1st matrix** must equal the number of **rows of the 2nd matrix**.
- And the result will have the same number of **rows as the 1st matrix**, and the same number of **columns as the 2nd matrix**.
In case of column or row vectors, if we want to multiply on the right by some [[Vector Matrix Form|column vector]], the result is a new column vector that is the combination of the column of the matrix and the rows of the vector, see:
$$
\begin{bmatrix}a&b&c \\ d&e&f \\ g&h&i\end{bmatrix}
\cdot
\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix}
= 
\begin{bmatrix}3(a,d,g) \\ 4(b,e,h) \\ 5(c,f,i)\end{bmatrix}
$$
The multiplication of a matrix by a column vector is the multiplication of each **row** of the vector by each **column** of the matrix, resulting in a new column vector.

Same goes for **row vectors** on t, each column of the row vector is multipled 