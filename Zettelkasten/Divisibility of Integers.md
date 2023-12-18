---
tags: number-theory
---
If $a$ and $b$ are integers with $a \ne 0$, we say that $a$ *divides* $b$ if exists a integer $c$ such that $b = ac$, because:
$$\begin{align*}
a,b &\in \mathbb{Z} \land \frac{b}{a} \in \mathbb{Z}\\
\therefore \exists c&\in \mathbb{Z} \;s.t\; (b=ac)\\
\because \frac{b}{a}&= c \therefore b=ac
\end{align*}$$ 
>Let $n$ and $d$ be positive integers, how many positive integers **not exceeding** $n$, are divisible by $d$ ?

We know that if some number $m$ is divisible by $d$, we have: $d | m \implies m = dk$ with $d \ne 0$ and $k \in \mathbb{Z}$. So the following holds:
$$\begin{align*}
0 &\lt m \le n\\
0 &\lt dk \le n\\
0 &\lt k \le \frac{n}{d}
\end{align*}$$
> [!attention] Corollary
> So there exists $\lfloor \frac{n}{d} \rfloor$ positive integers divisible by $d$ not exceeding $n$.      

## Properties of Divisibility

Let $a,b,c \in \mathbb{Z}$ where $a \ne 0$
1. If $a \mid b$ and $a \mid c$, then $a \mid (b + c)$.
$$\begin{align*}
a \mid b &\implies b=am, m \in \mathbb{Z}\\
a \mid c &\implies c= an, n \in \mathbb{Z}\\
b + c&= am + an\\
b + c &= a(m+n) \implies a \mid (b+c)\\
\therefore a &\mid (b+c)
\end{align*}$$
2. If $a \mid b$, then $a \mid bc \;\;\forall c \in \mathbb{Z}$.
$$\begin{align*}
a \mid b &\implies b=am, m \in \mathbb{Z}\\
bc &= amc\\
bc &= a(mc)\\
\therefore a &\mid bc
\end{align*}$$
3. If $a \mid b$ and $b \mid c$, then $a \mid c$.
$$\begin{align*}
a \mid b &\implies b=am, m\in \mathbb{Z}\\
b \mid c &\implies c=bn, n \in \mathbb{Z}\\
\therefore bc&= ambn\\
c &= amn\\
c&= a(mn)\\
\therefore a &\mid c.
\end{align*}$$
1. If $a \mid b$ and $a \mid c$, then $a \mid mb + nc$ for $m,n \in \mathbb{Z}$.
   From $(1)$ we know $a \mid mb, m\in \mathbb{Z}$ 
   From $(1)$ we know $a \mid nc, n\in \mathbb{Z}$ 
   Therefore from $(2)$ we know $a \mid mb + nc$.
 