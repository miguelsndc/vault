---
tags: number-theory
---
If $a$ and is a integer and $p$ is a [[Prime Numbers|prime]] number such that $a$ **does not divide** $p$, then:
$$\begin{align*}
a^{p-1}\equiv1\pmod{p}
\end{align*}$$
and
$$\begin{align*}
a^{p}\equiv a\pmod{p}
\end{align*}$$
Fermat's little theorem is pretty much an identity, with these two rules we can find remainders of numbers raised to huge powers, by decomposing them and finding those that are congruent module one, $a^{p-1}$ is a [[Modular Multiplicative Inverse]] of $a \mod p$.