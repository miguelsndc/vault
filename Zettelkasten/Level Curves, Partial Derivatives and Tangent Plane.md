---
tags: calculus
---
## How to visualize functions of several variables ? 

Plotting functions of three of more variables is impossible, so we stick to functions of two variables, $f(x,y)=z$. There exists some options to visualize them:
1. Plot the graph with $x,y$ and $z$ axis, but the difficulty of drawing such functions grows immensely depending on the complexity of the given function.
2. **Countor plot**:
A Countour plot of a given function $f$ shows all the points where $f(x,y)=c$ for some constant $c$, $i.e$ $f(x,y)=1$ $f(x,y)=2$ and so on, it works by intersecting a plane $z=c$ on the function and plotting the intersection points outlining the level on the final plot, it works like a **map**, telling you **how high** things are, the **elevation being the value of $z$**:

> Those points that are outlined when intersected by horizontal planes are called **level curves** of $f$ at a certain level $c$.

![[countor-plot.excalidraw]]

It is very easy to find values of $f$, given an input $(x,y)$, depending on the location of the input we can easily see that it is between $1$ and $2$ or $3$ and $2$ and so on. 

## Partial Derivatives

When looking at the countor plot it's easy to see how the function $f$ changes when $x$ or $y$ change, by simply looking at the values as you move towards one of the directions. However **how fast** $f(x,y)$ change is a trickier question, and **how fast** calls for *rate of change*, the [[Derivative Definition|derivatives]], in this case, the **partial derivatives**. 

Because $x$, $y$ or *both* variables can change, a special type of derivative is required, called the **partial derivative**, it is partial because it deals with one variable at a time. We fix one of the variables as a **constant** and see how the function changes with respect to the other variable, applying the same rules of differentation we are used to, denoted $\frac{\partial f}{\partial x}$.

**Geometrically** it means that at a certain point $(x_{0},y_{0})$ we fix *(let's assume the derivative is taken with respect to $x$ in this example.)*, we let $y$ be constant. This implies that at the point $(x_{0},y_{0})$. $y_{0}$ is **fixed**, and we **only move in the plane $y=y_{0}$ parallel to the xz plane**.
The curve is **sliced** by that plane, and the **slope of that sliced part of the curve, $z=f(x,y_{0})$ is $\frac{\partial f}{\partial x}$**, same for $(\partial f)/(\partial)$


![[Pasted image 20241030103658.png]]