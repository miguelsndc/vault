---
tags: matrix
aliases: elimination
---
Let $A$ be a $m\times n$ [[Matrix Definition|matrix]] of coefficients of a [[Definition of a System of Linear Equations|system]] $Ax = b$, our purpose is to eliminate numbers to make our system easier to solve.
- We accept the first equation is *okay*, and take the first number in the first row as the **pivot**, the number used to eliminate another number in a lower column.
$$
A = \begin{bmatrix}1 & 2  & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{bmatrix}
$$
To eliminate the $3$ at $A_{21}$ we got to multiply our **pivot row** by a constant $k$ that, when the $A_{2}$ row gets **subtracted** from our $kA_{1}$ it makes the first column $0$. That numbers is $3$, because: $3 - 3 = 0$, subtract the other columns as well to keep the system.

- Now we follow along with $A = \begin{bmatrix}1 & 2  & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1\end{bmatrix}$, now we have out pivot at $A_{22} = 2$, we aim to eliminate $A_{32}=4$, hence we multiply the row $A_{2}$ by $2$ and subtract from $A_{3}$, now we obtain $A = \begin{bmatrix}1 & 2  & 1 \\ 0 & 2 & -2 \\ 0 & 0 & 5\end{bmatrix}$, which notice it's a [[Upper Triangular Matrix]];
