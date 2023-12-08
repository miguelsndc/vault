---
tags: derivatives
---
Implicit differentation is a technique used to find [[Derivatives]] of [[Implicit and Explicit forms of a Equations|implicit]] equations, *notice we must assume $y$ is a [[Functions in Discrete Math|function]] of $x$*.
Hence we can find tangent lines and solve derivative problems in implicitly defined curves that **aren't functions**. To achieve so, we **derive** both sides of this equation in respect to $x$, and everywhere we derive a $y$ we add a $\frac{dy}{dx}$ or $y'$. See:

$$\begin{align*}
x^{2}+y^{2}&= 100\\
\frac{d}{dx}[x^2+y^{2}&= \frac{d}{dx}[100]\\
2x+2y \frac{dy}{dx}&= 0\\
\frac{dy}{dx}=\frac{-x}{y}
\end{align*}$$
Recall that if we wish to do something on one side of a [[Equation]] we must do it in the other side to preserve equality, the same thing applies for derivatives.

Hence we can find tangent lines on any $(x,y)$ point, on things that aren't functions, notice that we already do this, but in a explicit way:
$$\begin{align*}
y&= 4x^{3}+2x^{2}+x+23\\
\frac{d}{dx}[y]&= \frac{d}{dx}[4x^{3}+2x^{2}+x+23]\\
\frac{dy}{dx}&= 12x^{2}+4x+1 =y'
\end{align*}$$
This is the derivative of $y$, $\frac{dy}{dx}$ is just some fancy notation.