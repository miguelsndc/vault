---
tags:
  - avlc
aliases:
  - line
date: 2023-11-14
---
Different from the [[Cartesian Line Equation]], the parametric line equation lies on the idea that we can scale or shrink vectors infinetly. If we have a point and a vector, we can determine a arbitrary point that falls on this line by arbitrating values on a [[vault/content/S1/AVLC/Scalar|scalar]] $t$ that will grow or shrink the [[vault/content/S1/AVLC/Vector|vector]] to reach the desired points. 

We need two things: **two points**, since we can a take a vector out of them, or **a point and vector**, and then we basically have everything we need. The equation takes the form:
$$
(x,y,z)=(A,B,C)+t(a,b,c)
$$
Where the capital letters are the coordinates of the points, and the lowercase are the vector's endpoints and $t \in \mathbb{R}$. See an example:

> Find the parametric equation that passes by $A=(2,1,3)$ and $B(3,1,6)$

$$\begin{align*}
\vec{AB}&= B-A\\
\vec{AB} &= (1,0,3)
\end{align*}$$
Now we choose either $A$ or $B$ to be our reference point: (Choosing $A$)
$$\begin{align*}
(x,y,z)=(2,1,3)+t(1,0,3)
\end{align*}$$

