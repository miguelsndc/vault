___
Function composition is the act of "composing" (no shit), or *nesting* functions together, and evaluate from inside out if necessary, Let $f(x)$ and $t(x)$:

$$
\begin{align*}
f(x) &= x^{2}-1\\
t(x) &= \frac{3x}{2}
\end{align*}
$$

If we compose these functions with arbitrary values we can visualize the output in two manners:
$$\begin{align*}
f(t(4)) &= (t(4))^{2}- 1
\end{align*}$$
Or we can evaluate $t(3)$ first and plugin the result later on:
$$\begin{align*}
t(4) &= \frac{3\cdot4}{2}=\frac{12}{2}=6\\
f(6)&= 6^{2} - 1=36 -1=35
\end{align*}$$
Just choose whatever suits better

