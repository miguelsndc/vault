---
tags: integrals, derivatives
---
By knowing a [[Derivative Definition|derivative]], of any order and a result, like $y(\alpha) = \beta$, for the derivative one order up. we can find the unique function such that these constraints are met. Since [[Functions with the same derivative will differ by a constant]] by specifying the constant, the function is discretized from the others. 

$$\begin{align*}
\begin{cases}
\frac{dy}{dx}=2t-1\\
y(0)=1
\end{cases}
\end{align*}$$
*Find $y=y(x)$*
$$\begin{align*}
\frac{dy}{dx}=2t-1 \iff y(x)=\int 2t-1\;dt=t^{2}-t+C\\
\end{align*}$$
Also $y(0)=1 \iff C=1$, therefore $y(x)=t^{2}-t+1$.
This is extremely useful in some physics problems.