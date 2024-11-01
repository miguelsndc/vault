---
tags: calculus
---
## Optimization Problems (Maximization / Minimization) of functions of several variables

Let's figure out how to use [[Level Curves, Partial Derivatives and Tangent Plane|partial derivative]]s to handle optimization problems, partial derivatives monitor changes of a multivariable function choosing one to differentiate with respect to, while treating the others as constant. $\frac{\partial f}{\partial x}=f_{x}$ 

**Approximation Formula**

The linear approximation formula for single variable [[Functions in Discrete Math|function]]s around a certain point, works by finding the $1$st order taylor polynomial near that point, that is, **we match** the first [[Derivative Definition|derivative]] of our approximation with the first derivative of the given function, so we get a really close approximation around that point.

For multivariable functions you might already have an intuition for the approximation, since partial derivatives vary one variable and treat the others as constant, the effect of all changes add up and the function rate of change is approximated, by varying $x$ by a certain $\Delta x$ and $y$ by a certain $\Delta y$, then if $z=f(x,y)$, then $\Delta z$ around $z$ is $\Delta z = f_{x} \Delta x + f_{y}\Delta y$. By the same principles discussed before, the biggest difference is that we need to add up the partial derivatives to obtain the total change.

**Tangent Plane Approximation**

To justify the linear approximation formula above we can think in terms of the **tangent plane** to the surface at a given point. We saw that the partial derivatives give the slope of the tangent line at a point of the curve sliced by a plane parallel to the axis of **change**. 

Taking the partial derivative of each axis at that point give us two lines, and those lines are tangent to the point in question and are enough to define the tangent plane at that point as well.
___
Let's figure out the equations of those lines, the **slopes** at the point of tangency are respectively $f_{x}$ and $f_{y}$, so that means that, for $x$, if we fix $y=y_{0}$, and use $z$ as a function of $x$, the equation of the line tangent to the point is:
$$\begin{align*}
\begin{cases}
z=f_{x}(x_{0},y_{0})(x-x_{0})\\
y=y_{0}
\end{cases}
\end{align*}$$