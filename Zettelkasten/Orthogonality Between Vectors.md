---
tags:
  - vector
aliases:
  - orthogonal vector
  - orthogonal
date: 2023-11-02
---
> Recall that Orthogonality means: *"Intersecting or lying at right triangles"*

Two vectors $u$ and $v$ are orthogonal if and only if the [[Scalar Product]] between them **equals $0$**.
Because, recall from the [[Vector Norm|cauchy-schwarz inequality]], that:
$$\begin{align*}
 \cos(\theta)&=  \frac{u \cdot v}{||u|| \cdot ||v||} \\
\end{align*}$$
And if $\theta = 90\degree$, the $\cos(90\degree)=0$, it follows that:
$$\begin{align*}
\frac{u\cdot v}{||u|| \cdot ||v||}=0 
\end{align*}$$
Since [[Vector Norm|magnitude]] are always positive, and denominator of fractions can't equal $0$, it follows that the numerator is $0$ instead, so:
$$
u \cdot v = 0
$$
