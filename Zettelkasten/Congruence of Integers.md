---
tags: number-theory
---
If $a,b \in \mathbb{Z}$ and $n \in \mathbb{Z}$, we say that $a$ and $b$ are **congruent** modulo $n$ if $a \bmod n = b \bmod n$, in other words, if $a$ and $b$ have the same remainder when divided by $n$, so the notation is:
$$\begin{align*}
a \equiv b \pmod n \iff a \bmod n =b \bmod n
\end{align*}$$
Another useful result is also that $a \equiv b \; (\bmod n) \iff n \mid (a-b)$. 

> [!important] Theorem
> Let $m$ be a positive integer. The integers $a$ and $b$ are congruent modulo $m$ if and only if there is a integer $k$ such that $a = b + km$.
## Proof
If $a \equiv b \pmod m$ then $m \mid a - b$, so there exists $k \in \mathbb{Z}$ such that $a - b = km$, so that $a = b + km$. [[Converse]]ly, if $a=b+km$, then $km=a-b$, hence, $m\mid km$ which implies that $m\mid(a-b)$.
# Properties of Congruence
1. Let $m \in \mathbb{Z}$, if $a \equiv b \pmod n$, and $c \equiv d \pmod n$ then $a+c \equiv b+d \pmod n$.
We know $a \equiv b \pmod n \implies m \mid a - b$, and $c \equiv d \pmod n \implies m \mid c - d$, Since
(I) $m \mid a - b \implies a - b = mk$ for $k \in \mathbb{Z}$, so $a = b + mk$.
(II) $m \mid c - d \implies c - d= mq$ for $q \in \mathbb{Z}$, so $c + d + mk$.
Since (I) and (II) holds, we can add them to form:
$$\begin{align*}
a + c &= b +d+mq+mk\\
a + c &= b+d+m(q + k)
\end{align*}$$
Therefore, $a+c \equiv b + d \pmod n$.
1. Let $m \in \mathbb{Z}$, if $a \equiv b \pmod n$, and $c \equiv d \pmod n$ then $ac \equiv bd \pmod n$.
Similarly to $(1)$ we have:
(I) $a \equiv b \pmod m \implies m \mid a - b \implies a = b+mk$ for $k \in \mathbb{Z}$
(II) $c \equiv d \pmod m \implies m \mid c - d \implies c = d+mq$ for $a \in \mathbb{Z}$
Since (I) and (II) holds, we can multiply them to obtain:
$$
\begin{align*}
a&= b+mk\\
c&= d + mq\\
ac &= (b + mk)(d+mq)\\
ac &= bd + bmq + mkd + m^{2}kq\\
ac &= bd + m(bq + kd + mkq)
\end{align*}
$$
So it holds that $ac \equiv bd \pmod n$. 