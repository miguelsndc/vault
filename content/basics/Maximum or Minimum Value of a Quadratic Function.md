---
tags:
  - quadratics
date: 2023-10-13
source: "[[James Stewart Precalculus.pdf]]"
page: 247
aliases:
  - maximum value
  - minimum value
---
Let $f$ be a [[Quadratic Function]] in the [[Standard Form of a Quadratic Function|standard form]], The **maximum** or **minimum** value of $f$ occurs at $x = h$.
- If $a \gt 0$, then the **minimum value** of $f$ is $f(h) = k$
- If $a \lt 0$, then the **maximum value** of $f$ is $f(h) = k$
The maximum or minimum value or a function $f$ in the form $f(x) = ax^{2}+bx+c$ occurs at:
$$\begin{align*}
x=-\frac{b}{2a}
\end{align*}$$
- If $a\gt 0$ Then the min value is $f(- \frac{b}{2a})$ 
- If $a\lt 0$ Then the max value is $f(- \frac{b}{2a})$
##### Proof
This $- \frac{b}{2a}$ thing seems arbitrary, but it actually can be found by [[Completing the Square]] of the function $f(x) = ax^{2}+bx+c$. See:
$$\begin{align*}
f(x)&= ax^{2}+bx+c\\
f(x)&= a\left(x^{2} + \frac{b}{a}x\right)+c\\
(\frac{\frac{b}{a}}{2})^{2}&= \frac{b^{2}}{4a^{2}}\\
f(x)&= a\left(x^{2}+ \frac{b}{a}x + \frac{b^{2}}{4a^{2}}\right)+c-a\left(\frac{b^{2}}{4a^{2}}\right)\\
f(x) &= a\left(x + \frac{b}{2a}\right)^{2}+c - \frac{b^{2}}{4a} 
\end{align*}$$
This function is in the standard form with $h = - \frac{b}{2a}$ and $k = c - \frac{b^{2}}{4a}$ 