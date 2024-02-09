---
tags: derivatives
---
Theorem: Let $f(x)$ be a differentiable function, then:
- $f(x) = x^{n} \implies f'(x) = nx^{n-1}$
- $f(x)= x^{-n}\implies f'(x) = -nx^{-n-1}$
- $f(x)= x^{\frac{1}{n}} \implies f'(x) = \frac{1}{x} x^{\frac{1}{n}-1}$
## Proofs
Using the [[Epsilon-Delta Definition of a Limit|limit]] definition of a [[Derivative Definition|derivative]]:
(I): $f(x) = x^{n} \implies f'(x) = nx^{n-1}$, so $f'(x) = \lim_{h\rightarrow0} \frac{(x+h)^{n}-x^{n}}{h}$ , Let $x+h = t$ such that $t \rightarrow x\implies h \rightarrow 0$. So we have:
$$\begin{align*}
f'(x)&= \lim_{t\rightarrow x} \frac{t^{n}-x^{n}}{t-x}\\
&= \lim_{t\rightarrow x} t^{n-1}+t^{n-2}x+t^{n-3}x^{2} + \cdots +x^{n-1} \;\; n \text{ times}\\
&= x^{n-1}+ x^{n-2}x+x^{n-3}x^{2}+ \cdots + x^{n-1}\\
&= x^{n-1}+x^{n-1}+x^{n-1}+\cdots+x^{n-1}\\
&=nx^{n-1}
\end{align*}$$
So $f(x) = x^{n}\implies f'(x)= nx^{n-1}$, examples are: $f(x)= x^{3}\implies f'(x) =3x^{2}$, $f(x)= 4x^{5}\implies f'(x)=20x^{4}$.
___
(II): $f(x) = x^{-n}\implies -nx^{-n-1} \;?$, using the [[Derivative Definition]], this is: $\lim_h\rightarrow0 \frac{(x+h)^{-n}-x^{-n}}{h}$ So we have:
$$\begin{align*}
f'(x) &= \lim_{h\rightarrow0} \frac{(x+h)^{-n}-x^{-n}}{h}\\
&= \lim_{h\rightarrow0} \frac{\frac{1}{(x+h)^{n}}- \frac{1}{x^{n}}}{h}\\
&= \lim_{h\rightarrow0}  \frac{x^{n} - (x+h)^{n}}{h}\cdot \frac{1}{(x+h)^{n}x^{n}}\\
&= \lim_{h\rightarrow0}  -\frac{(x+h)^{n} - x^{n}}{h}\cdot \frac{1}{(x+h)^{n}x^{n}}\\
\text{ By (I), }\lim
\end{align*}$$

