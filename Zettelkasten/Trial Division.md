---
tags: number-theory
---
> [!example] Conjecture 
> If $n$ is a [[Prime Numbers|composite]] integer, then $n$ has a [[Prime Numbers|prime]] divisor less than or equal to $\sqrt{n}$.

This is used when performing a prime test, to check whether a number is prime or not. Other than doing by brute force and checking all numbers up to $n$, we can check this number against all primes $p$ $s.t$ $p \le \sqrt {n}$,  no further tests are necessary, it this passes, then $p$ is prime.

## Proof
We want to prove that if $n \in \mathbb{Z}$ then $n=ab$ for $a,b \in \mathbb{Z}$ where $1 \lt a \lt n$ and $b > 1$, then $a \le \sqrt{n}$ and $b \le \sqrt{n}$.
We'll use a proof by [[Contradiction|contradiction]], suppose $a \gt \sqrt{n}$ and $b \gt \sqrt{n}$. Since $a>1$ and $b>1$ we can multiply the [[Inequality]] together, so:
$$\begin{align*}
ab \gt n\\
n \gt n
\end{align*}$$
Which forms a contradiction.