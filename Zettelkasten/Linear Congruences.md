---
tags: number-theory
---
Equations arise in many scenarios, also in modular arithmetic, see, the question: *"Which number that, when multiplied by three and divided by five leaves remainder two ?"* can be expressed as a **linear congruence**:
$$\begin{align*}
3x \equiv 2 \pmod{5}
\end{align*}$$
This equation has *infinitely many* solutions and will be every number of the form $x=5k+4$. We can solve such equations by finding a [[Modular Multiplicative Inverse]], a number such that when multiplied by both sides of the congruence leaves remainder $1$ on the $x$ side. This way we can isolate the $x$, it can usually be found by either **thinking a little harder** of doing the [[Extended Euclidean Algorithm]] to find the [[Bezout Coefficients]], and the inverse will be exactly the number multiplying the constant $3$.
