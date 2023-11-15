---
tags:
  - avlc
aliases: 
date: 2023-11-15
---
With [[Parametric Line Equation|parametric lines]] we use a [[vault/content/S1/AVLC/Vector|vector]] and a point to determine the line. As such:
$$\begin{align*}
x&= x_{0}+at\\
y&= y_{0}+bt
\end{align*}$$
Where $x_{0},y_{0}$ are constants and $t\in \mathbb{R}$ is the parameter.
We can eliminate the parameter by multiplying the upper equation by $b$ and the bottom by $a$ and subtract them to obtain $ay-bx=ay_{0}-bx_{0}$. Noticing the second member is a constant, we replace it by $c$:
$$\begin{align*}
ay-bx=c
\end{align*}$$
Which is called the **Cartesian Equation** of the line $r$. if $a\ne 0$ we can divide the equation by $a$ and get $$y=\frac{b}{a}x + \frac{c}{a}$$By letting $m=\frac{b}{a}$ and $k = \frac{c}{a}$ we have: $y=mx+k$ where $m=\frac{b}{a} = \tan{\theta}$. And $m$ is called the [[vault/content/basics/Average Rate of Change|slope]] of the line.
By letting $A=b$, $B=-a$ and $C=-c$ we have: $$Ax +By+C=0$$Which is the **standard form of the line**. If $(x_{0},y_{0})$ is a point of the line, then:
$$
\begin{align*}
Ax_{0}+By_{0}+C&= 0
\end{align*}
$$
By subtracting  $Ax_{0}+By_{0}+C=0$ from $Ax+By+C=0$ We get:
$$\begin{align*}
A(x-x_0)+B(y-y_0)=0
\end{align*}$$
>Interpreting this as a [[vault/content/S1/AVLC/Scalar Product|Scalar Product]] between vectors $(A,B)$ and $(x-x_0,y-y_0,z-z_0)$, we see that the solutions for this are all points $(x,y)$ where those vectors are [[vault/content/S1/AVLC/Orthogonality Between Vectors|orthogonal]] to each other, meaning this line contains $(x_0,y_0)$ and has the direction of vector $(-B,A)$