---
tags: derivatives
---
Theorem:
- $f(x) = \rm{e}^{x}\implies f'(x)=\rm{e}^{x}$ 
- $g(x) = \ln{x} \implies g'(x)= \frac{1}{x}$
- $f(x)=a^{x}\implies f'(x)=a^{x}\ln{a}$.
- $f(x)=\log_{a}x \implies f'(x)=\frac{1}{x\ln{a}}$.
## Proofs
$f(x) = \rm{e}^{x}\implies f'(x)=\rm{e}^{x}$:
$$\begin{align*}
f'(x)&= \lim_{h\rightarrow0} \frac{\rm{e}^{(x+h)} - \rm{e}^{x}}{h} \\
&= \lim_{h\rightarrow0} \frac{\rm{e}^{x}\rm{e}^{h}-e^{x}}{h}\\
&= \lim_{h\rightarrow0} e^{x}\cdot \lim_{h\rightarrow0}\frac{e^{h}-1}{h}
\end{align*}$$
By the [[Fundamental Exponential Limits]], $\lim_{h\rightarrow0}\frac{e^{h}-1}{h} = 1$, so the [[Derivative Definition|derivative]] of $f(x)=e^{x}$ is $f'(x)=e^{x}$.
___
$g(x) = \ln{x} \implies g'(x)= \frac{1}{x}$
$$\begin{align*}
g'(x)&= \lim_{h\rightarrow0} \frac{\ln(x+h) - \ln{x}}{h}\\
&= \lim_{h\rightarrow0} \frac{1}{h}\cdot \ln\left[1+ \frac{h}{x}\right]
\text{ Let } u=\frac{h}{x}\\
&= \lim_{u\rightarrow0} \ln(1+u)^\frac{1}{xu}\\
&= \lim_{u\rightarrow0} \frac{1}{x} \ln(1+u)^{\frac{1}{u}}\\
&= \lim_{u\rightarrow0} \frac{1}{x}\cdot \ln{e}\\
&= \frac{1}{x}
\end{align*}$$
___
$f(x)=a^{x}\implies f'(x)=a^{x}\ln{a}$.
$$\begin{align*}
f'(x)&= \lim_{h\rightarrow0} \frac{a^{(x+h)}-a^{x}}{h}\\
&= \lim_{h\rightarrow0}a^{x}\cdot \frac{a^{h}-1}{h}\\
&= a^{x} \cdot\ln{a}
\end{align*}$$
> $[e^{x}]'=e^{x}$ only because $\ln{e}=1$.
___
$f(x)=\log_{a}x \implies f'(x)=\frac{1}{x\ln{a}}$.

Therefore: 
- $[e^{x}]'=e^{x}$ 
- $[\ln{x}]'=\frac{1}{x}$ 