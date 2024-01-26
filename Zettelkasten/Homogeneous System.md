---
tags: systems, spaces
---
A [[Definition of a System of Linear Equations|system of linear equations]] having a [[Matrix Definition|matrix]] form of $Ax=\vec{0}$, where $\vec{0}$ represent a **zero [[Column Matrix]]** is called a **Homogeneous System**.
The solution set for a homogeneous system is always a vector [[Linear Subspaces|subspace]], hence they are one of the primary ways to represent vector subspaces. 
Consider the system:
$$\begin{align*}
S &= \Bigg\{(x,y,z)\in \mathbb{R}^{3}\mid
\theta\begin{cases}
x+2y+z=0\\
2x-2y+z=0\\
\end{cases} 
  \Bigg\}
\end{align*}$$
$S$ is a subspace described by the system $\theta$. There's three types of solution sets possible:
1. Unique solution
In this case one single [[Vector]] represent the solution for the system. For example, a ton of lines intersecting at a single point. For this to happen the **number of equations and variables must be equal**, the equations must be **consistent** and there must be no  [[Linear (In)dependence.|linear dependence]] between any two or more equations.
1. Infinitely many
This is the case where we have a [[Linear (In)dependence.|linear dependence]] between some of the equations, or the [[Rank of a Matrix|rank]] of the [[Augmented Matrix]] $A$ is less than the number of variables *or columns*, then we get a pivotless column and/or a column with all zeroes, both representing a free variable. Usually when the system has equations than variables *but not always*.
1. No solution
When the equations are unconsistent, something like $x+y= 2$ and $2x+2y=3$, the system has no solution.