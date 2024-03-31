---
tags: integration-techniques
aliases: power rule
---
Let $f(x) = x^{n}$ the [[Derivative Definition|derivative]] of $f$ is simply $f'(x) = nx^{n-1}$ according to the general [[Derivative Power Rule]]. To integrate $f(x)= x^{n}$, one must notice that the exponent of the antiderivative is $n+1$, since $x$ is a standalone term we must also divide by $n+1$, so it becomes $\int f(x) \, dx = \frac{x^{n+1}}{n+1} \because \frac{d}{dx}\left[\frac{x^{n+1}}{n+1}\right]=x^{n}$.

[[Antiderivative of a function|antiderivative]] of $x^{a}$ with $a \ne -1$ and $a$ constant will go as follows:
$$\begin{align*}
\frac{d}{dx}\left[\frac{1}{a+1}x^{a+1}\right]=x^{a}, \implies \int x^{a}dx&= \frac{x^{a+1}}{a+1}+C
\end{align*}$$
___
$\rm{Examples}$
- $\int x^{3}dx$ 
  $$\begin{align*}
\int x^{3}dx&= \frac{x^{4}}{4} \because \frac{d}{dx}\left[\frac{x^{4}}{4}\right]=x^{3}
\end{align*}$$
- $\int \frac{1}{x^{2}}dx$
  $$\begin{align*}
\int \frac{1}{x^{2}}dx=\int x^{-2}dx=\frac{x^{-2+1}}{-2+1}=-x^{-1}=\frac{-1}{x}+C
\end{align*}$$
