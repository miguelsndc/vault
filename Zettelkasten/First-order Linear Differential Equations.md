---
tags: differential-equations
aliases: first-order, linear
---
We understand a linear [[Differential Equation|differential equation]] to be a equation whose unknown function and it's derivative have at most degree $1$, defined as:
$$\begin{align*}
(1) \;\;\;\;\; \frac{dx}{dt}=xg(t)+f(t)
\end{align*}$$
Where $g$ and $f$ are [[Differentiability and Continuity|continuous]] functions defined in some [[Intervals|interval]] $I$. If we let $f(t) =0$, then $(1)$ becomes [[Equações Diferenciais Separáveis de 1a Ordem|separable]], $\frac{d}{dx}=xg(t)$, and the general solution is:
$$\begin{align*}
\frac{dx}{dt}&= xg(t)\\
\frac{dx}{x}&= g(t)dt\\
\int \frac{1}{x}dx &= \int g(t) d(t)\\
\ln(x)+K&= G(t)dt+K'\\
\ln(x)&= K+G(t)dt\\
e^{\ln(x)}&= e^{K+G(t)dt}\\
x&= Ke^{G(t)}, k \in \R
\end{align*}$$Where $G(t)$ is a [[Antiderivative of a function|antiderivative]] of $g$ and notice we have replaced every constant term with $K$ multiple times.

Now let's solve when $f(t) \ne 0$. Notice that:
$$\begin{align*}
\frac{d}{dt}[x\rm{e}^{-\int g(t)\,dt}]
\end{align*}$$
