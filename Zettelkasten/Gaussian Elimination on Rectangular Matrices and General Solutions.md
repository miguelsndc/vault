---
tags: systems, spaces
---
## Overall
Suppose the $m$ by $n$ matrix $A$ is reduced by elementary operations and [[Row Exchanges]] to a matrix $U$ in [[Echelon Form]]. Let there be $r$ non-zero [[Pivot|pivots]]; the last $m-r$ rows of $U$ are zero. Then there will be $r$ *basic variables* and $n-r$ *free variables,* correspoding to the rows of $A$ with and without pivots, respectively.
The [[Nullspace]], formed of solutions to $Ax = 0$, has the $n-r$ free variables as independent parameters. If $r=n$, there are no free variables and the nullspace contains only $x=0$.
Solutions exist for every right side $b$ if and only f $r=m$; with this number of pivots, the matrix $U$ has no zero rows, and $Ux=c$ can be solved by [[Back-Substitution]]. In case $r \lt m$, $U$ will have $m-r$ zero rows and there are $m-r$ constraints on $b$ in order for $Ax=b$ to be solvable; they appear explicitly in the last $m-r$ rows of $Ux=c$. If one particular solution exists then every other solution differs from it by a vector in the nullspace of $A$.
*The number $r$ is called the [[Rank of a Matrix|rank]] of $A$.*
 ___
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
U&= 
\begin{pmatrix}
1 & 3 & 3 & 2\\
0 & 0 & 3 & 1\\
0 & 0 & 0 & 0 
\end{pmatrix}
\end{align*}$$
Elimination is complete, Notice $A$ is in a upper *"trapezoid"* form, since all non-zero entries $u_{ij}$ lie above the main diagonal. Notice its on [[Echelon Form]].
There is [[A = LU Factorization]] just as in square matrices, but $L$ is square of order $3$, the same number of rows in $A$ and $U$:
$$\begin{align*}
L&= 
\begin{pmatrix}
1 & 0 & 0\\
2 & 1 & 0\\
-1 & 2 & 1\\
\end{pmatrix}
\end{align*}$$
In this specific case, no [[Row Exchanges]] were needed, this would include a [[Permutation Matrix|permutation matrix]] $P$, that'd need to be carried on $A$ in order to get $PA = LU$.

> [!Tip] General Theorem
> For every $m \times n$ rectangular $A$ there is some [[Permutation Matrix]] $P$, a [[Lower Triangular Matrix]] $L$ with unit diagonals and a upper trapezoid $U$ in [[Echelon Form]] such that $PA = LU$.

