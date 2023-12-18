---
tags: number-theory
---
If $a$ and $b$ are integers with $a \ne 0$, we say that $a$ *divides* $b$ if exists a integer $c$ such that $b = ac$, because:
$$\begin{align*}
a,b &\in \mathbb{Z} \land \frac{b}{a} \in \mathbb{Z}\\
\therefore \exists c&\in \mathbb{Z} \;s.t\; (b=ac)\\
\because \frac{b}{a}&= c \therefore b=ac
\end{align*}$$
> [!faq] Question
> Let $n$ and $d$ be positive integers, how many positive integers **not exceeding** $n$, are divisible by $d$ ?

We know that if some number $m$ is divisible by $d$, we have: $d | m \implies m = dk$ with $d \ne 0$ and $k \in \mathbb{Z}$. So the following holds:
$$\begin{align*}
0 &\lt m \le n\\
0 &\lt dk \le n\\
0 &\lt k \le \frac{n}{d}
\end{align*}$$
So there exists $\lfloor{}$   