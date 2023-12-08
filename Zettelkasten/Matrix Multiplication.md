---
tags: matrix
aliases: multiplication, matrix multiplication, multiply, multiplying
---
>[!bug] Remember
>Matrix multiplication is **not** commutative.

To multiply two [[Matrix Definition|matrices]], apply the [[Scalar Product|dot product]] between the rows of the one on **the left** and the **columns** of the one on the right, it will be the $k$ columns of the row multiplied each by the row in the column of the other matrix and **summed up**, that's why columns in $A$ must equal rows in $B$, if $B$ is a column matrix there are no values to sum after, so we just multiply and put each in a new column in $C$.

$$
C_{ij}=a_{i1}b_{1j} +a_{i2}b_{2j}+\cdots+ a_{im}b_{mj}=\sum_{k=0}^{m}a_{ik}b_{kj}
$$

- The number of **columns of the 1st matrix** must equal the number of **rows of the 2nd matrix**.
- And the result will have the same number of **rows as the 1st matrix**, and the same number of **columns as the 2nd matrix**.
- Matrix multiplication is **associative** (fancy word for: "we can move the parentheses").

>[!danger] Important
> To do **row operations** we multiply a matrix on the left, to do **column operations** we multiply on the right.

>[!tip] Tip
> To multiply an **m×n** matrix by an **n×p** matrix, the **n**s must be the same,  
and the result is an **m×p** matrix.

In case of column or row vectors, multiply on the right by some [[Vector Matrix Form|column vector]], the result is a new column vector whose components are the column of the matrix and the rows of the vector, see:
$$
\begin{bmatrix}a&b&c \\ d&e&f \\ g&h&i\end{bmatrix}
\cdot
\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix}
= 
\begin{bmatrix}3(a,d,g) \\ 4(b,e,h) \\ 5(c,f,i)\end{bmatrix}
$$
The multiplication of a matrix by a column vector is the multiplication of each **row** of the vector by each **column** of the matrix, resulting in a new column vector.

Same goes for **row vectors**.