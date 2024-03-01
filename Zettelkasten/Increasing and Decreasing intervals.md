---
tags: functions, derivatives
---
The growth of [[Functions]] can be described by the [[Derivative Definition|derivatives]], Let $f$ be [[Differentiability and Continuity|differentiable]] on a interval $(a,b)$.
- $f$ is  ***strictly** increasing* if $s \lt t \implies f(s) \lt f(t)$ 
- $f$ is ***strictly** decreasing* if $s < t \implies f(s) \gt f(t)$, $\forall s \forall t \in (a,b)$.

As a consequence of the [[Mean Value Theorem]]: Let $f$ [[Differentiability and Continuity|continuous]] on some [[Intervals|interval]] $I$
- $\rm{I}$ If $f'(x) \gt 0 \; \forall x \in I$, $f$ is strictly increasing.
- $\rm{II}$ If $f'(x) \lt 0 \; \forall x \in I$, $f$ is strictly decreasing.
## Proof
$\rm{I}$. We must show that for any $s,t \in I$, $s \lt t \implies f(s) \lt f(t)$, so, let $s,t \in I$ with $s \lt t$. By the [[Mean Value Theorem]], since $f$ is [[Differentiability and Continuity|differentiable]] and [[Differentiability and Continuity|continuous]] on $I$, there exists $x$ such that:
$$\begin{align*}
f(t) - f(s)=f'(x)(t-s)
\end{align*}$$
Since $t \gt s$ and $f'(x) \gt 0$ by hypothesis, it follows that $f'(x)(t-s) \gt 0$, therefore $$\begin{align*}
f(t) - f(s) \gt 0 \implies f(s) \lt f(t)
\end{align*}$$
Therefore $\forall s \forall t \in I, s \lt t \implies f(s) \lt f(t)$.
___
$\rm{II}$ Proof is analogous to $\rm{I}$. We must show that $s \lt t \implies f(s) \gt f(t)$ $\forall s \forall t \in I$. Let $f$ be [[Differentiability and Continuity|differentiable]] and [[Differentiability and Continuity|continuous]] on $I$, so there exists $y$ such that:

$$\begin{align*}
f(t) - f(s) &= f'(y)(t-s)
\end{align*}$$
Since $f'(y) \lt 0$ by hypothesis, $f'(y)(t-s) \lt 0$. Therefore:
$$\begin{align*}
f(t)-f(s) \lt 0 \implies f(s)\gt f(t)
\end{align*}$$
And we are done.