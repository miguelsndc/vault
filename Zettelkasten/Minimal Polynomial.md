---
tags: eigen-everything, polynomials
---
A *minimal* [[Polynomials|polynomial]] of a [[Linear Transformations|transformation]] or [[Matrix Definition|matrix]] $A$ is a [[Monic Polynomials|monic]] polynomial $m$ such that:
$$\begin{align*}
m(x) &= x^{k}+a_{k-1}x^{k-1}+\cdots+a_{0}
\end{align*}$$
and 
- $m(A) = \vec{0}$, that is, $m(x)$ annihilates $A$.
- It's the polynomial with the **least degree** amongst those who annihilate $A$.

Given a matrix $A$, $A$ [[Diagonalizable Matrices|diagonalizable]] [[If and Only if]], the *minimal polynomial* of $A$:
$(x - \lambda_{1})(x - \lambda_{2})\cdots(x - \lambda_{r})$ annihilates $A$. Instead of calculating all the [[Eigenvalues and Eigenvectors|eigenvalues]] and [[Eigenvalues and Eigenvectors|eigenvectors]] to only then know if $A$ is diagonalizable, we can perform this test to figure it out without having to calculate the eigenvalues.