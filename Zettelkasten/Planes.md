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