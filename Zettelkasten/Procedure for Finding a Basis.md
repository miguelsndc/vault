---
tags: spaces
---
To find a [[Theorems and Proofs for Basis and Dimension|basis]] of a [[Vector Space]] one must:
1. Find the [[Augmented Matrix]] $M$
2. Put $M$ in [[Row Reduced Echelon Form]] 
3. If [[Rank of a Matrix|rank]] of $M$ is equal to the number of columns then the vectors are linearly independent and already form a basis. Otherwise, [[Parameterization of Rectangular System's Solutions|parameterize]] the solutions and write it in terms of the parameters.
4. Throw in some fancy notation
Example:
Find a basis for $S = \Bigg\{(x,y,z) \in R^{3}\mid \begin{cases} x+y+2z= 0 \\ 2x - y = 0 \end{cases} \Bigg\}$. We can already see by the concept of [[Theorems and Proofs for Basis and Dimension|dimension]] that whatever basis $S$ has, it will be a single vector spanning a line, but anyway it goes like:
$$\begin{align*}
&\begin{pmatrix}1 & 1 & 2\\
2 & -1 & 0\end{pmatrix}
\implies
\begin{pmatrix}
1 & 1 & 2\\
0 & -3 & -4
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 1 & 2 \\
0 & 1 & \frac{4}{3}\end{pmatrix}\\
&\implies
\begin{pmatrix}
1 & 0 & \frac{-1}{3} \\
0 & 1 & \frac{4}{3}\end{pmatrix} 
\end{align*}$$
[[Row Reduced Echelon Form|row reduced]] form checked. The parameterization is:
$$\begin{align*}
\begin{cases}
x &= -\frac{1}{3}t\\
y &= - \frac{4}{3}t\\
z=t 
\end{cases}
\;\;\;\;\;\,,t\in\mathbb{R}
\end{align*}$$
So a basis for $S$ is $(\frac{-1}{3},\frac{-4}{3},1)$.

It goes the same for Polynomials and Matrices, you just gotta do some more work to translate the restrictions to a [[Augmented Matrix]] but the thing really goes the same, with matrices, you can assign every cell to a row in a [[Vector Matrix Form|column vector]] and operate, with polynomials the only difference are the plus signs and the unknowns that are really arbitrary and dont impact on anything.

