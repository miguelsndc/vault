---
tags: vector
aliases:
  - line
  - parametric line equations
  - parametric line
  - parametric lines
---
We can understand lines as [[Intersection]] of [[Planes]], we have seen that planes can intersect at a line at that [[Definition of a System of Linear Equations|system]] represents the line in space. 
There's another way to think about it: as the **trajectory of a moving point** in space, moving at constant speed on the line. This trajectory can be expressed as a [[Functions|function]] of time, where $Q(t)$ represents where the point is at time "$t$".
Let $Q_{0} = (1,2,2)$ be the starting point, i.e, $t=0$, and $Q_{1}=(2,1,3)$ when $t=1$.
![[parametric_line.excalidraw]]
> What's the position at time $Q(t)$ ?

To answer the question we can first notice that the vector $\vec{Q_{0}Q_{1}}$ represents a displacement, from $Q_{0}$, of $Q_{0}Q_{1}$; and that happens when $t=1$. The vector $\vec{Q_{0}Q(t)}$ is, safely, exactly $t \cdot \vec{Q_{0}Q_{1}}$.

$Q(t)$ can be thought of as having each coordinate as a function of $t$: $Q(t) = (x(t), y(t), z(t))$
And so the vector $Q_{0}Q(t)$ is:
$$\begin{align*}
\begin{cases}
x(t) - 1 &= t\\
y(t) - 2 &= -t\\
z(t) - 2 &= t
\end{cases}
\end{align*}$$
We are extracting a vector $Q_{0}Q(t)$ by letting $Q_{0}Q(t)=Q(t)-Q_{0}$  be some multiple of $Q_{0}Q_{1}=(1,-1,1)$. Or more conveniently:

$$\begin{align*}
\begin{cases}
x(t) &= 1+ t\\
y(t) &= 2-t\\
z(t) &= 2+t
\end{cases}
\end{align*}$$
Namely, the point $Q(t)$ is the displacement $t$ from $Q_{0}$ of $t \cdot Q_{0}Q_{1}$.