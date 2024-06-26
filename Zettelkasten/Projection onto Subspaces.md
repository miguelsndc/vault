---
tags: linear-transformations,vector,matrix
aliases: projections
---
>[!faq] The Formula
> To project a [[Vector|vector]] $b$ onto [[Linear Subspaces|subspace]], first define a [[Matrix Definition|matrix]] $A$ whose columns are the [[Theorems and Proofs for Basis and Dimension|basis]] vectors of that subspace, then use $P = A(A^{T}A)^{-1}A^{T}$ to obtain the projection matrix, then simply do $\proj{b}{\im{A}}=Pb$.

___
# The Idea
**Why project ?**
First, projections are useful to find solutions to linear [[Definition of a System of Linear Equations|systems]], and most of the time these systems *don't have solutions*, that means, for $Ax = b$, $b$ is not in the [[Image of a linear transformation|column space]] of $A$, most of the time.
So instead, solving the *closest problem* to this one gives us a way to approximate the solution by projecting $b$ onto $\im{A}$ and given some error $e$, we can find the best solutions for $A$, $i.e$ instead of solving $Ax = b$, we solve $Ax = p$, where $p$ is the projection.
## Derivation
Let's find a formula for projecting a vector onto a [[Plane]], that is, if the plane is the column space of $A$ in $Ax=b$, and $b$ is not in it, we'll project $b$ there. So given two vectors $a_{1}, a_{2}$ that [[Span|span]] the [[Image of a linear transformation|column space]] of $A$ (the plane), projecting $b$ there means that there is some error $e$ such that $e = b - p$ and $e$ is [[Orthogonal Vectors|orthogonal]] to the plane, that is, $e \perp a_{1}$ and $e \perp a_{2}$.

Instead of doing everything through [[Linear Combinations|linear combinations]], we'll find a matrix that does the projection. So, let $A = [a_{1},a_{2}]$, a matrix whose columns are the [[Theorems and Proofs for Basis and Dimension|basis]] for the plane, we can confidently say that the column space of $A$ is the plane. 

So, we know that $p$, our projection, is a combination of $a_{1}$ and $a_{2}$, like $p = \hat{x}_{1}a_{1} + \hat{x}_{2}a_{2}$, but we are really running away from this definition, instead, let's say that $p$ is the matrix $A$ times some number $\hat{x}$ we don't really know, $p= A\hat{x}$. Then the error $e$ is $b - A\hat{x}$. We also know that $e$ must be orthogonal to $a_{1}$ and $a_{2}$ so:
$$\begin{align*}
{a_{1}}^{T}(b-A\hat{x})=0 \;\; {a_{2}}^{T}(b-A\hat{x})=0
\end{align*}$$
This can also be written as:
$$\begin{align*}
\begin{pmatrix}
{a_{1}}^{T}\\
{a_{2}}^{T}
\end{pmatrix}(b-A\hat{x})=0
\end{align*}$$
However this is just equal to $A^{T}$, therefore we have:
$$\begin{align*}
A^{T}(b-Ax)=0
\end{align*}$$
Which implies that $e$ is orthogonal to $A^{T}$, since $A^{T}e$ is in the [[Kernel of a linear transformation|null space]] of $A^{T}$, and the nullspace of $A^{T}$ is [[Orthogonal Vectors|orthogonal]] to the [[Image of a linear transformation|column space]] of $A$, therefore $e$ is orthogonal to the column space of $A$ and also orthogonal to the whole plane! Now we just solve for $\hat{x}$:
$$\begin{align*}
A^{T}(b- A\hat{x})&= 0\\
A^{T}b-A^{T}A\hat{x}&= 0\\
A^{T}A\hat{x}&= A^{T}b\\
(A^{T}A)^{-1}(A^{T}A)\hat{x}&= (A^{T}A)^{-1}A^{T}b\\
\hat{x}&= (A^{T}A)^{-1}A^{T}b
\end{align*}$$
Since $p= A\hat{x}$, and we've found $\hat{x}$, $p$ therefore is:
$$\begin{align*}
p&= A(A^{T}A)^{-1}A^{T}b\\
\text{Let }P&=  A(A^{T}A)^{-1}A^{T}\\
\therefore p&= Pb
\end{align*}$$
And that's the projection of $b$ onto the column space of $A$.
## Disclaimer and Geometric interpretation
Notice that if we develop $(A^{T}A)^{-1}$ we find out that $P$ is the [[Identity Matrix]], so something should be wrong right ?
Notice that $A$ being invertible means that $A$ is a [[Square Matrix]]. Since we're in $n$-dimensional space and $A$ is a matrix whose columns are [[Theorems and Proofs for Basis and Dimension|basis]] vectors for the [[Linear Subspaces|subspace]] being projected onto, if $A$ is square, $A$ is $n \times n$ and therefore $A$ [[Span|span]]s the whole $n$-dimensional space. Projecting a vector onto the space it already belongs, it's just the vector itself, and $A$ being the identity makes sense.