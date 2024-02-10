---
tags: derivatives
---
Theorem:
- $f(x) = \rm{e}^{x}\implies f'(x)=\rm{e}^{x}$ 
- $g(x) = \ln{x} \implies g'(x)= \frac{1}{x}$
## Proofs
$f(x) = \rm{e}^{x}\implies f'(x)=\rm{e}^{x}$:
$$\begin{align*}
f'(x)&= \lim_{h\rightarrow0} \frac{\rm{e}^{(x+h)} - \rm{e}^{x}}{h} \\
&= \lim_{h\rightarrow0} \frac{\rm{e}^{x}\rm{e}^{h}-e^{x}}{h}\\
&= \lim_{h\rightarrow0} e^{x}\cdot \lim_{h\rightarrow0}\frac{e^{h}-1}{h}
\end{align*}$$
By the [[Fundamental Exponential Limits]], $\lim_{h\rightarrow0}\frac{e^{h}-1}{h} = 1$, so the [[Derivative Definition|derivative]] of $f(x)=e^{x}$ is $f'(x)=e^{x}$.