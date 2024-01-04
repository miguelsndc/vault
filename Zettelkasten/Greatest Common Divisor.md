---
tags: number-theory
---
>[!tip] Definition
>Let $a$ and $b$ be integers, not both zero. *The largest integer $d$ such that $d \mid b$ and $d \mid a$* is denoted by $\gcd(a,b)$.

The $\gcd$ can be found by either [[Prime Numbers|prime]] factorization and then just finding by eye the common largest, or by the following:
$$\begin{align*}
&\gcd(a,b) :\\
a&= p_{1}^{a_{1}} \cdot p_{2}^{a_{2}} \cdots p_{n}^{a_{n}},\\
b&= p_{1}^{b_{1}} \cdot p_{2}^{b_{2}} \cdots p_{n}^{b_{n}},\\
\end{align*}$$
Where the exponents are nonnegative integers and the primes are present in both factorizations, Therefore:
$$\begin{align*}
\gcd(a,b)&= p_{1}^{\min(a_{1},b_{1})} \cdot p_{2}^{\min(a_{2},b_{2})} \cdots p_{n}^{\min(a_{n},b_{n})}
\end{align*}$$
## Example:
Because $120=2^{3}\cdot 3 \cdot 5$, $500 = 2^{2}\cdot 5^{3}$
$$\begin{align*}
\gcd(120, 500)&= 2^{\min(3,2)}\cdot 3^{\min(1, 0)} \cdot 5^{\min(3,1)}\\
&= 20
\end{align*}$$
