---
tags: derivatives
---
Theorem: Let $f(x)$ be a differentiable function, then:
- $f(x) = x^{n} \implies f'(x) = nx^{n-1}$
- $f(x)= x^{-n}\implies f'(x) = -nx^{-n-1}$
- $f(x)= x^{\frac{1}{n}} \implies f'(x) = \frac{1}{x} x^{\frac{1}{n}-1}$
## Proofs
Using the [[Epsilon-Delta Definition of a Limit|limit]] definition of a [[Derivative Definition|derivative]]:
$f(x) = x^{n} \implies f'(x) = nx^{n-1}$, so $f'(x) = \lim_{h\rightarrow0} \frac{(x+h)^{n}-x^{n}}{h}$ , Let $x+h = t$ such that $t \rightarrow x\implies h \rightarrow 0$. So we have:
$$\begin{align*}
f'(x)&= \lim_{t\rightarrow x} \frac{t^{n}-x^{n}}{t-x}\\
&= \lim_{t\rightarrow x} t^{n-1}+t^{n-2}x+t^{n-3}x^{2}

\end{align*}$$
