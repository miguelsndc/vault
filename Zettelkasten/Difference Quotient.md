---
tags: derivatives
---
The Difference Quotient is a formula that explains how a [[Functions in Discrete Math|function]] $f$ behaves in a interval from $x$ to $x+h$ where $h$ is a arbitrary [[Real Numbers]]. Notice that both are in the [[Domain]] of $f$.
We aim to find the [[Average Rate of Change]] of the function from $f(x)$ to $f(x+h)$, to do so, we apply the formula and obtain:
$$\begin{align*}
\frac{f(x+h) - f(x)}{h}
\end{align*}$$
This operation denotes how this function behaves from $x$ to $x+h$ and we divide by $h$ to obtain the average change. 
If we take smaller and smaller values of $h$, *but never zero*, we start to notice the graph of this other function converge from two points to one point as $h$ get arbitrarily small, at some point it becomes **tangent** to the original point of $x$. This limiting behaviour allows us to determine the behavior of the function **at a specific point**, the idea of **instantaneous rate of change** comes to mind, although this sounds really paradoxal, that's what it is.
By letting $h$ approach zero we find:
$$
\lim_{h\to0}\frac{f(x+h)-f(t)}{h}
$$Which is indeed the instantenous rate of change of $f$. between $x$ and $x+h$, since we let $h\to 0$, it's pretty much the change from $x$ to $x$, or, **no change at all in $x$**. we are fucking calculating the change at one single point, if we apply this to a function, we get what is called the [[Derivative]] of this function.