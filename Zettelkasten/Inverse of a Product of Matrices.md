---
tags: matrix
---
Let $A$ and $B$ be invertible [[Matrix Definition|matrices]], the matrix that represents the [[Inverse Matrix|inverse]] of the [[Matrix Multiplication|product]] of these two, is the product of the inverses, in reverse order. See:
$$
A\cdot B \cdot B^{-1} A^{-1} = I
$$
We can take advantage of the fact that matrices are associative, and do:
$$\begin{align*}
A \cdot (B \cdot B^{-1}) \cdot A^{-1}&= I\\
A \cdot I \cdot A^{-1} &= I \\
I \cdot A^{-1}&= I\\
I&= I
\end{align*}$$
And we it's hence proved.
The other way around couldn't be shown because matrices aren't commutative, and we **could not** commute the matrices in order to get $M\cdot M^{-1}$ where $M$ is arbitrary, and we are **stuck**.
$$\begin{align*}
A \cdot B \cdot A^{-1}\cdot B^{-1}=I
\end{align*}$$
There's not much to do here.