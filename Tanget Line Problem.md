---
tags:
  - calc
  - limits
date: 2023-11-11
---
The word tangent is derived from the Latin *tangens* that means "touching", Thus a tangent line to a curve is a line that touches that curve and should have the same direction of it in the point of contact.

Thus if we want to find a tangent line to a curve, If the curve is a circle, we can just follow euclides and say that a tangent line touches a circle once and only once.

But for other curves this is not so precise. See:

![[Tanget Line Problem.excalidraw]]

Here we have the lines $l$ and $t$. We clearly see that $t$ is not what we would call a tangent line, $l$ looks more promising though, but it touches the curve twice. Let's try to find the tangent line of a parabola $y=x^2$.
____
## Finding the Tangent line

> Find the [[Linear Equation]] of the tangent line that crosses the function $y=x^{2}$ at the point $P(1,1)$.

We know that we can find the equation of a line as soon as we find it's [[Average Rate of Change|slope]] $m$. The whole problem is that we only know one point $P$, whereas we need two points to calculate the slope. But see we can compute an **approximation** to $m$ by picking a random point $Q(x,x^{2})$ and calculating the slope $m_{pq}$ of the **secant line** $PQ$. for $x\ne 1$ and $Q \ne P$ we have:
$$\begin{align*}
m_{pq}&= \frac{x^{2}-1}{x-1} 
\end{align*}$$
As an example, for the point $Q(1.5,2.25)$ we obtain:
$$\begin{align*}
m_{pq}&= \frac{2.25-1}{1.5-1}=\frac{1.25}{0.5}=2.5
\end{align*}$$
Notice that for several values of $x$ close to $1$:

| $x$   | $m_{pq}$ |
| ----- | -------- |
| $2$     | $3$        |
| $1.5$   | $2.25$     |
| $1.1$   | $2.1$      |
| $1.01$  | $2.01$    |
| $1.001$ | $2.001$    |  

| $x$   | $m_{pq}$ |
| ----- | -------- |
| $0$     | $1$        |
| $0.5$   | $1.5$     |
| $0.9$   | $1.9$      |
| $0.99$  | $1.99$    |
| $0.999$ | $1.999$    |  

See that the closer $Q$ is to $P$, the closer $x$ is to $1$, the closer $m_{pq}$ is to $2$. This suggests that the slope of the tangent line $l$ should be $m=2$. 
We say that the slope of the tanget line is the [[Limits|limit ]]of the slopes of the secant lines, and we express this symbolically by writing:
$$\begin{align*}
&\lim_{Q \to P} m_{pq}= m\\
&\lim_{x\to 1}= \frac{x^{2}-1}{x-1}=2 
\end{align*}$$
Assuming that the slope of the tangent line is $m=2$ we can use the [[Point-Slope Equation of Line]] to write the equation of the tangent line:
$$\begin{align*}
y-1 =2(x-1)&= 2x-1
\end{align*}$$
