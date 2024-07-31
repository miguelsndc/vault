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
Seja a equação $(1)\;\;\ \frac{d}{dx}= g(t)h(x)$ em que $g$ e $h$ são funções definidas em intervalos abertos $I_{1}$ e $I_{2}$ com $g$ contínua em $I_{1}$ e $h'$ contínua em $I_{2}$. Assim, se $x=x(t),t \in I$, for solução **não** constante de $(1)$, então, $\forall t \in I, h(x(t)) \ne 0$.

Suponha que $x=x(t), t \in I$ é uma solução não constante de $(1)$, assim, para todo $t \in I$,
$$\begin{align*}
x'(t) &= g(t)h(x(t))
\end{align*}$$
ou
$$\begin{align*}
\frac{x'(t)}{h(x(t)}&= g(t)
\end{align*}$$
Seja $J = \{x(t) \mid t \in E\}$; $J$ é um intervalo pois $x=x(t)$ é [[Differentiability and Continuity|contínua]]. Observemos que para todo $x \in J, \,\, h(x) \ne 0$. A função $\frac{1}{h(x)}$ sendo contínua em $J$ admite uma [[Antiderivative of a function|primitiva]] $H(x)$, neste intervalo, $H'(x) = \frac{1}{h(x)}, x \in J$, segue que, para todo $t \in I$:
$$\begin{align*}
[H(x(t))]'=g(t)
\end{align*}$$
Seja $G(t)$ uma primitiva de $g$ em $I$, segue do teorema que existe uma constante $k$ tal que, para todo $t \in I$:
$$\begin{align*}
H(x(t))=G(t)+k
\end{align*}$$
Como $h(x) \ne 0$ em $J$ e por $h$ ser contínua, segue que $\frac{1}{h(x)}$ mantém o mesmo sinal em $J$. Logo $H$ é estritamente decrescente ou estritamente crescente em $J$, e portanto, **inversível**. Seja $H^{-1}$ a inversa de $H$ em $J$, concluímos que:
$$
\begin{align*}
x(t) &= H^{-1}(G(t)+k)
\end{align*}

$$