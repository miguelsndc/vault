---
tags: systems
---
When the number of equations in a [[Definition of a System of Linear Equations|system]] differ the number of unknowns $A_{m\times n}$ and $m \ne n$, $Ax=b$, [[Gaussian Elimination]] proceeds normally, but attention is needed on [[Back-Substitution]].
*Ex:* Look at the [[Scalar|scalar]] equation $ax=b$ a humble $1\times1$ system, we have three possibilities of solutions:
1. If $a \ne 0$ there is a unique solution $x=\frac{b}{a}$, this is the [[Non-Singular Case Matrix of a System|non-singular]] case.
2. If $a=0$ and $b=0$. There are infinitely many solutions, since $0x=0$ is true for any $x$ this is the *underdetermined* case.
3. If $a = 0$ and $b\ne0$, There's **no** solution for $ax=b$, this is the **unconsistent** case.
For [[Square Matrix]] all three cases are possible, but for [[Rectangular Matrices]], only cases $2$ and $3$ apply.
___
Consider the $3 \times 4$ [[Matrix Definition|matrix]]: 
$$\begin{align*}
A &= 
\begin{pmatrix}
1 & 3 & 3 & 2\\
2 & 6 & 9 & 5\\
-1 & -3 & 3 & 0\\
\end{pmatrix}
\end{align*}$$
Perfoming regular elimination $A$ becomes:
$$\begin{align*}
A&= 
\begin{pmatrix}
1 & 3 & 3 & 2\\
0 & 0 & 3 & 1\\
0 & 0 & 6 & 2
\end{pmatrix}
\end{align*}$$
If A were a square matrix, this would mean that $A$ is [[Singular Case in Square Matrices Ax = b|singular]], but since $A$ is rectangular, all we can do is continue the elimination and go on to the next column, where the pivot is non-zero. 

$$\begin{align*}
A&= 
\begin{pmatrix}
1 & 3 & 3 & 2\\
0 & 0 & 3 & 1\\
0 & 0 & 0 & 0 
\end{pmatrix}
\end{align*}$$
Elimination is complete, Notice $A$ is in a upper *"trapezoid"* form, since all non-zero entries $u_{ij}$ lie above the main diagonal. It has some "staircase" or "echelon" form, Like:
$$\begin{align*}
\begin{pmatrix}
* & * & * & * & * & * & * & * & * \\
0 & * & * & * & * & * & * & * & * \\
0 & * & * & * & * & * & * & * & * \\
* & * & * & * & * & * & * & * & * \\
* & * & * & * & * & * & * & * & * \\
\end{pmatrix}
\end{align*}$$