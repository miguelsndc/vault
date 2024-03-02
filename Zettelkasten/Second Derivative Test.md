---
tags: functions, derivatives
---
Let $f$ be a [[Functions in Discrete Math|function]] [[Differentiability and Continuity|differentiable]] up to $2$nd order on some [[Intervals|interval]] $I$.
- If $f''(x) \gt 0$ in $I$, then $f$ is [[Concavity|concave up]] in $I$
- If $f''(x) \lt 0$ in $I$, then $f$ is [[Concavity|concave down]] in $I$.
[[Inflexion Points]] can be found through setting $f''(x)$ to $0$ and finding points where $f''$ either equals $0$ or does not exist, once found, one can test points *within those intervals* and the **sign of those points** will determine the sign for the whole interval. That's the second derivative test.
## Proof
Let $p$ be a [[Real Numbers|real]] in $I$, we must prove that for any $x \in I$, $x\ne p$:
$$\begin{align*}
f(x) \gt T(x)
\end{align*}$$
Where $T(x)=f(p) + f'(p)(x-p)$.
Let $g(x) = f(x) - T(x)$, we'll prove that $g(x) \gt 0 \; \forall x \in I$. We have
$$\begin{align*}
\begin{cases}
g'(x)=f'(x)-T'(x)\\
T'(x)=f'(p)
\end{cases}
\end{align*}$$
So $g'(x) = f'(x) - f'(p)$. Since $f''(x) \gt 0$ by hypothesis, it follows that $f'(x)$ is [[Increasing and Decreasing intervals|strictly increasing]] in $I$, so:
$$\begin{align*}
\begin{cases}
g'(x) \gt 0 \text{ for } x \gt p\\
g'(x) \lt 0 \text{ for } x \lt p\\
\end{cases}
\end{align*}$$
it follows that $g$ is [[Increasing and Decreasing intervals|strictly decreasing]] in $\{x \in I \mid x \lt p\}$ and [[Increasing and Decreasing intervals|strictly decreasing]] in $\{x \in I \mid x \gt p\}$, since $g(p) = 0$, this results in $g(x) \gt 0$ for all $x \in I \; x \ne p$.

The other proof is analogous.