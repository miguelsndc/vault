---
tags: matrix
---
> [!tip] Definition 
> Let $A_{m\times n}$ be a [[Matrix Definition|matrix]], the **inverse** of $A$ will be that matrix whose [[Matrix Multiplication|multiplication]] by $A$ will yield the [[Identity Matrix]], we call it $A^{-1}$, the inverse 
> of $A$.
> 
> Invertible Matrices are called **Non-Singular**
> Non-Invertible Matrices are called **Singular**

Square matrices $A$, if it is invertible, then $A\cdot A^{-1}=I=A^{-1}\cdot A$, this won't happen for non-square matrices since the rules don't allow it, but for squares this works.

> A [[Square Matrix]] $A$ won't have a inverse if a can find a non-zero [[Vector|vector]] $v$ where $Av=0$.
## Proof
Suppose a **non-zero** vector $v$ and a matrix $A$ where $Av=0$.
Assume $A$ is invertible, then it has a inverse $A^{-1}$, so:
$$\begin{align*}
Av&= 0\\
A^{-1}Av=0\\
Iv=0\\
v=0
\end{align*}$$
For this inverse to exist, $v$ should equals zero, but it doesn't, so we have a [[Contradiction|contradiction]] therefore $A$ can't have an inverse if $Av =0$.

