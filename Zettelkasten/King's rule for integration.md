---
tags: integrals
---
This technique for definite [[Antiderivative of a function|integrals]] uses the fact that the *area under a curve is always the same whether you evaluate from $a$ to $b$ or from $b$ to $a$*, it looks like:
$$\begin{align*}
\int_{a}^{b} f(x) \, dx
&= \int_{a}^{b} f(a+b-x) \, dx
\end{align*}$$
It just does a bunch on translations and reflections in the graph and brings it back to the same place.
## The actual method
Let's compute $\int^{\frac{\pi}{2}_{0}} \frac{1}{1+ (\tan{x})^{\pi}} \, dx$.
- First, label the integral $I$ and use the king's property:
$$\begin{align*}
I &= \int^{\frac{\pi}{2}_{0}} \frac{1}{1+ (\tan{x})^{\pi}} \, dx\\
&= \int^{\frac{\pi}{2}_{0}} \frac{1}{1+ (\tan(\frac{\pi}{2}-x))^{\pi}} \, dx\\
&= \int^{\frac{\pi}{2}}_{0} \frac{1}{1+ \frac{1}{(\tan{x})^{\pi}}}  \, dx\\
&= \int^{\frac{\pi}{2}}_{0} \frac{(\tan{x})^{\pi}}{(\tan{x})^\pi+1}  \, dx\\
&= \int^{\frac{\pi}{2}}_{0} \frac{(\tan{x})^{\pi}+1-1}{(\tan{x})^\pi+1}  \, dx\\
&= \int^{\frac{\pi}{2}}_{0} dx- \int^{\frac{\pi}{2}_{0}} \frac{1}{1+ (\tan{x})^{\pi}} \, dx\\
&= \frac{\pi}{2}-I\\
2I&= \frac{\pi}{2}\\
I&= \frac{\pi}{4}
\end{align*}$$
