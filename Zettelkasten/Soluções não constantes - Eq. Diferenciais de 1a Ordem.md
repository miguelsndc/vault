---
tags: differential-equations
---
Seja a equação $\frac{d}{dx}= g(t)h(x)$ definidas em [[Intervals|interval]]os abertos $I_{1}$ e $I_{2}$, com $g$ [[Differentiability and Continuity|continua]] em $I_{1}$ e $h'$ contínua em $I_{2}$, então:
$$\begin{align*}
\frac{d}{dx}&= g(t)\,\,h(x) \;\;\;\;\;(\delta) \\ 
\frac{dx}{h(x)}&= g(t)\,dt\\
\int \frac{dx}{h(x)}&= \int g(t)\,dt\\
H(x) &= G(t)+ k\\
x&= H^{-1}(G(t)+ k)
\end{align*}$$
com $x = x(t)$ sendo uma solução de $\delta$.
____
## Prova

> [!tip] Teorema
Seja a equação $(1) \frac{d}{dx}= g(t)h(x)$ em que $g$ e $h$ são funções definidas em intervalos abertos $I_{1}$ e $I_{2}$ com $g$ contínua em $I_{1}$ e $h'$ contínua em $I_{2}$. Assim, se $x=x(t),t \in I$, for solução **não** constante de $(1)$, então, $\forall t \in I, h(x(t)) \ne 0$.

Suponha que $x=x(t), t \in I$ é uma solução nã constante de  