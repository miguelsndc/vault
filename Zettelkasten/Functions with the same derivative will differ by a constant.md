---
tags: functions, derivatives
---
Let $f$ be [[Differentiability and Continuity|continuous]] on some [[Intervals|interval]] $I$. If $f'(x)=0$ for every $x \in I$, then there exists some constant $k$ such that $f(x)=k$ for every $x$ in $I$.
## Proof
Let $x_{0}$ be some point in $I$, we will show that $f(x) = f(x_{0})$, with $x \ne x_{0}$, this means, $f$ is constant. For all $x \in I, x \ne x_0$, exists, by the [[Mean Value Theorem]], some $x'$ in the open interval of extremes $x, x_{0}$ such that:
$$\begin{align*}
f(x)-f(x_{0})=f'(x')(x-x_{0})
\end{align*}$$
Since $x' \in I$, by hypothesis, $f'(x')=0$, so $f(x)-f(x_{0})=0 \implies f(x)=f(x_{0})$. Taking $f(x_{0})=k$, yields the theorem.

>[!ti] Corollary
>Let $f$ and $g$ be [[Differentiability and Continuity|continuous]] on $I$. If $f'(x)=g'(x) \;\; \forall x \in I$, then there exists some constant $k$ such that $g(x)=f(x)+k$, for all $x\in I$.
## Proof
The function $h(x) = g(x) - f(x)$ is [[Differentiability and Continuity|continuous]] in $I$ and for all $x \in I$, $h'(x) = g'(x)-f'(x) = 0$. So, *by the previous theorem*, $h(x)=k$, so $g(x)-f(x)=k \implies g(x) = f(x) + k$. which proves the corollary. 