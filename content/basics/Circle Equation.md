---
tags:
  - equations
  - geometry/analytic
date: 2023-09-20
source: "[[James Stewart Precalculus.pdf]]"
page: 98
---
The equation of a circle of with center $(h, k)$ and radius $r$ is , see: [[Graph of a Circle]]:
$$\begin{align*}
(x-h)^{2}+(y-k)^{2}&=r^2
\end{align*}$$
This is called the **standard form** of the circle, if the center is the origin $(0, 0)$, then it becomes:
$$\begin{align*}
x^{2}+y^{2}=r^{2}
\end{align*}$$
Take a circle with a center $C(3, 1)$ and a arbritrary radius of 67 and expand it, we get:
$$\begin{align*}
(x- 3)^{2}+(y-1)^{2}&= 67\\
x^{2}-6x +9+y^{2}-2y+1&= 67\text{ Subtract 10 from both sides}\\
x^{2}-6x+y^{2}-2y&= 67\\
x^{2}+y^{2}-6x-2y&= 67
\end{align*}$$
It's quite hard to see that this is circle. But look at $x$ factors $x^{2}, -6x$ and $y$ factors $y^{2},-2y$, we see , that they are both uncomplete [[Quadratic Equation]]s, that we can hence solve by [[Completing the Square]], once we get the remaining value for x and for y, we can put it into the standard form again. 

#### Deriving

By definition, a circle with center $C(h,k)$ and radius $r$ is the set of all points $P(x,y)$ whose distance from the center is the radius, $d(C,P) = r$, so, by the [[Distance Formula]] we have:
$$\begin{align*}
\sqrt{(x-h)^{2}+(y-k)^{2}}&= r\\
(x-h)^{2}+(y-k)^{2}&=r^2
\end{align*}$$
This is the desired equation.
