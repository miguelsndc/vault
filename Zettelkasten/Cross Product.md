---
tags: vectors
aliases: cross
---
The cross product is a binary operation that takes two [[Vector|vectors]] and produces a third vector, cross product is a *space* operation.

**Def:** $\vec{A} \times \vec{B}$ is a vector:
$$\begin{align*}
\det\begin{pmatrix}
\hat{i} & \hat{j} & \hat{k}\\
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_3
\end{pmatrix}&= \hat{i}\det\begin{pmatrix}a_{2} & a_{3}\\ b_{2} & b_{3}\end{pmatrix}- \hat{j}\det\begin{pmatrix}a_{1} & a_{3} \\ b_{1} & b_{3}\end{pmatrix}+\hat{k}\det\begin{pmatrix}a_{1} & a_{2} \\ b_{1} & b_{2}\end{pmatrix}
\end{align*}$$
As we can see is a [[Linear Combinations|linear combination]] of the basis vectors, therefore is also a vector.
___
- $\norm{\vec{A} \times \vec{B}}$ equals the **area of the parallelogram** created by $\vec{A}$ and $\vec{B}$ in space. 
- $\f{dir}(\vec{A} \times \vec{B})$ is [[Orthogonality|orthogonal]] to the plane of the parallelogram. Using the right-hand rule we determine whether it's perpendicular **up** or **down**.* 