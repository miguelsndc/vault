---
tags:
  - algebra
  - khan-academy
  - precalculus
  - functions
date: 2023-09-14
link: https://www.khanacademy.org/math/precalculus/x9e81a4f98389efdf:composite/x9e81a4f98389efdf:composing/v/function-composition
---
Function composition is the act of "composing" (no shit), or *nesting* functions together, and evaluate from inside out if necessary, Let $f(x)$ and $t(x)$:

$$
\begin{align*}
f(x) &= x^{2}-1\\
t(x) &= \frac{3x}{2}\\
\end{align*}

$$
Then if we compose $f(x)$ and $t(x)$:
$$
\begin{align*}
f(t(x)) &= \bigg(\frac{3x}{2}\bigg)^{2}-1\\
t(f(x)) &= \frac{3(x^{2}-1)}{2}
\end{align*}
$$
The formal defition is *which is read as "f composed with t"*:
$$\begin{align*}
(f \;\circ \;t)(x) &= f(t(x))
\end{align*}$$
___
If we compose these functions with arbitrary values we can visualize the output in two manners:
1. We can evaluate from inside out, taking the output of $t(4)$ and plugin the result on $f(x)$:
$$\begin{align*}
t(4) &= \frac{3\cdot4}{2}=\frac{12}{2}=6\\
f(6)&= 6^{2} - 1=36 -1=35
\end{align*}$$
2. We can find the total composite function, by following that:
$$\begin{align*}
f(t(x)) &= (t(x))^{2}- 1\\
f(t(x)) &= \bigg(\frac{3x}{2}\bigg)^{2}-1\\
f(t(x))&= \frac{9x^2}{4}-1
\end{align*}$$
	This function should take us directly to 35.

