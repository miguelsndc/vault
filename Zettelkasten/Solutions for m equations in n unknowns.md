---
tags: systems
---
When the number of equations in a [[Definition of a System of Linear Equations|system]] differ the number of unknowns $A_{m\times n}$ and $m \ne n$, $Ax=b$, [[Gaussian Elimination]] proceeds normally, but attention is needed on [[Back-Substitution]].
*Ex:* Look at the [[Scalar|scalar]] equation $ax=b$ a humble $1\times1$ system, we have three possibilities of solutions:
1. If $a \ne 0$ there is a unique solution $x=\frac{b}{a}$, this is the [[Non-Singular Case Matrix of a System|non-singular]] case.
2. If $a=0$ and $b=0$. There are infinitely many solutions, since $0x=0$ is true for any $x$ this is the *underdetermined* case.
3. If $a = 0$ and $b\ne0$, There's **no** solution for $ax=b$, this is the **unconsistent** case.
For [[Square Matrix]] all three cases are possible, but for [[Rectangular Matrices]] 