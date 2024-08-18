---
tags: vectors, geometry
aliases: plane, planes
---
A plane is a flat-surface in $3$-dimensional space, [[Span|span]]ned by two [[Vector|vectors]]. It is defined either parametrically with three points contained in the plane: $P_{0}, P_{1}$ and $P_{2}$, where we take the vectors $\vec{P_{0}P_{1}}$ and $\vec{P_{0}P_{2}}$, for example, and define the plane as all [[Linear Combinations|linear combination]]s of these two.
Or we can take a simpler approach, and define the plane as all vectors $P= \innp{x,y,z}$ such that the [[Dot Product|dot product]] between $P$ and a **normal** vector $\hat{n}$ is $0$, this means all vectors that are perpendicular to $\hat{n}$, thus forming a plane. if $\hat{n} = \innp{a,b,c}$ then the [[Equation]] of the plane is$ax+by+cz+d=0$. $d$ is a constant term that allows this definition to represent planes that don't pass through the origin.

**Example**:
> Give the equation of the plane $\pi$ with normal $\hat{n}=\innp{1,5,10}$ that passes through $P_{0}=(2,1,-1)$

Let $P = (x,y,z)$ be a point in space, the plane is formed by all vectors $\vec{P_{0}P}$ $s.t$ $\vec{P_{0}P}\cdot \hat{n}=0$ $i.e$ $\vec{P_{0}P} \perp \hat{n}$. So $\vec{P_{0}P} = \innp{x-2,y-1, z+1}$ and:
$$\begin{align*}
\hat{n} \cdot \vec{P_{0}P} &=\innp{1,5,10}\cdot\innp{x-2,y-1,z+1}=0\\
&= x-2+5(y-1)+10(z+1)=0\\
&= x-2+5y-5+10z+10=0\\
&= x+5y+10z+3=0
\end{align*}$$
Or we could have simply said all vectors $\vec{v}$ such that $\hat{n} \cdot v = \hat{n}\cdot \vec{OP_{0}}$ and since $\hat{n}\cdot \vec{OP_{0}}=3$, we let $d = 3$ and the equation is just $x+5y+10z+3=0$.
___
The constant $d$ **roughly** tell us how far we've moved from the origin; there is a special case when $\hat{n}$ is a [[Vector Normalization|unitary vector]], the constant $d$, if $\ne 0$ is **exactly the distance of the plane from the origin**.

Because if $\hat{n}$ is unitary then the component of any vector $OP$ from the origin to any point $P$ in the plane along the normal is exactly $OP \cdot \hat{n}$, since $\hat{n}$ is unitary:
$$\begin{align*}
ax+by+cz&=-d\\
OP \cdot n&= ax+by+cz\\
|OP\cdot n| &= |-d|\\
OP \cdot n &= |d|
\end{align*}$$
Since $OP \cdot n$ is the distance, $d$ is the distance also.
___
Planes can intersect in:
- A point.
- A line.
- A plane.
- or don't intersect at all.
if we're dealing with three planes, the [[Determinant in 2 dimensions|determinant]] of the normals $n_{1},n_{2},n_{3}$ will determine the type of intersection, if $\det(n_{1},n_{2},n_{3})\ne0$ then there exists a unique solution, since the matrix $M$ whose columns are the normals is [[Inverse Matrix|invertible]], thus $M$ is a [[Bijective Linear Transformations|bijective]] [[Linear Transformations|transformation]]

If $\det(M) = 0$ we can have either infinitely many solutions or no solutions at all, $n_{1},n_{2}$ and $n_{3}$ are **coplanar** because the volume of the parallelepiped formed is $0$. We can even take the [[Cross Product]] between two of them and determine the plane they're contained in the also the line, parametrically, with direction vector $n_{i}\times n_{j}$. We can either have the intersection of three different combinations of the same plane, and if it isn't, the line is contained in the planes;

