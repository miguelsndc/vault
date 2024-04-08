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
So instead, solving the *closest problem* to this one, let's us approximate the solution by projecting $b$ onto $\im{A}$ and given some error $e$, we can find 