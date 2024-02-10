---
tags: derivatives, limits
---
The [[Functions in Discrete Math|function]] $f(x)=|x|$ isn't *differentiable* in $p=0$; however, this function **is** [[Continuity of A Function|continuous]] in $p=0$. Which shows us that a function can be continuous at a point but not differentiable in this point; Which leads to two conclusions:
- Continuitiy does not imply differentiability
- However, **differentiability implies continuity**, as the following theorem states:
> Theorem: if $f(x)$ is differentiable in $p$, then $f(x)$ is continuous at $p$.
## Proof
$\lim_{x\rightarrow p} \frac{f(x)-f(p)}{x-p}=f'(p)$.
We need to show that $f(x)$ is continuous at $p$, this menans: $\lim_{x\rightarrow p } f(x)=f(p)$. We have:
$$\begin{align*}
\frac{f(x)-f(p)}{x-p} \cdot (x-p) =f(x)-f(p) \;\;\;(x \ne p)\\
\implies
\end{align*}$$
