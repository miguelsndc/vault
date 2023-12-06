---
tags: derivatives
---
Quick Cheatsheet for [[Derivatives]]:
- Derivation of a constant $c$: $\frac{d}{dx}(c)=0$    
- Power Rule: $\frac{d}{dx}(x^{n})=nx^{n-1}$
- Constant Multiple Rule: $\frac{d}{dx}[cf(x)]=c \frac{d}{dx} f(x)$.
- Sum and Difference Rules:
$$\begin{align*}
\frac{d}{dx}(f(x)+g(x))&= \frac{d}{dx}f(x) + \frac{d}{dx}g(x)\\
\frac{d}{dx}(f(x)-g(x))&= \frac{d}{dx}f(x) - \frac{d}{dx}g(x)
\end{align*}$$
- Product Rule: *if $f$ and $g$ are both differentiable [[Functions in Discrete Math|functions]], then*
$$\begin{align*}
\frac{d}{dx}[f(x)\cdot g(x)]&= \frac{d}{dx}[f(x)] \cdot g(x) + f(x) \cdot \frac{d}{dx}[g(x)]
\end{align*}$$
- Quotient Rule, *if $f$ and $g$ are both differentiable [[Functions in Discrete Math|functions]], then*:
$$\begin{align*}
\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right]&= \frac{\frac{d}{dx}[f(x)] \cdot g(x) - f(x) \cdot \frac{d}{dx}[g(x)]}{[g(x)]^{2}}
\end{align*}$$
