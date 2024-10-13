---
tags: algorithms
aliases: asymptotic
---
For a more informal review and definition, check the [[Asymptotic Notation]] page. Here we do crazy math formal bamboozling shit.
___
The notations we use to describe the asymptotic running time of an algorithm are defined in terms of [[Functions|functions]] from the [[Sets|set]] $\N$ of natural numbers to the set $\R$ of [[Real Numbers]], these definitions have shown convenient for analyzing running times.
## $O$-Notation
$O$-notation describes an **asymptotic upper bound**. We use $O$ notation to give an upper bound on a function, to within a costant factor. For a given function $g(n)$, we denote $O(g(n))$ the set of functions:
$$\begin{align*}
O(g(n))=\{f(n)\mid \exists c \gt 0\exists n_{0} \forall n&\ge n_{0}: 0 \le f(n) \le cg(n)\}
\end{align*}$$
A function $f(n)$ belongs to the set $O(g(n))$ if there exists a positive constant $c$ such  that $f(n)\le cg(n)$ for sufficiently large $n$ *(sufficiently large being $n \ge n_{0}$)*.

The above definition of $O(g(n))$ requires $f(n)$ to be **asymptotically nonnegative**, that is $f(n) \ge 0$ for sufficiently large $n$, *(An **asymptotically positive** function is one that is positive for all sufficiently large $n$)*. Consequently, the function $g(n)$ itself must be asymptotically nonnegative, or else the set $O(g(n))$ is empty.

We usually write $f(n) = O(g(n))$ to indicate that $f(n)$ belongs to $O(g(n))$, you might expect that we would write $f(n) \in O(g(n))$ *which is technically correct*, however describing asymptotical behaviours as equations has it's own advantages, We'll show that $4n² +100n+500n = O(n^{2})$,

> By abusing notation and using equations instead of set operators we can use inequalities and other mathematical gotchas to prove way more easily the asymptotic behaviour of a function $f(n)$ given $O(g(n))$.

We need to find positive constants $c$ and $n_{0}$ such that: *$n_{0}$ replaces $n$*
$$\begin{align*}
4n^{2}+100n+500n &\le cn^{2}\\
4 + \frac{100}{n} + \frac{500}{n^{2}}&\le c\\
\begin{cases}
n_{0}=1\implies604&\le c\\
n_{0}=10\implies19&\le c\\
\vdots
\end{cases}
\end{align*}$$
We've shown that $f(n)=O(n^{2})$ with constants $n_{0}=10$ and $c=19$.

## $\Omega$-Notation
Just as $O$-notation provides an asymptotic *upper bound* on a function, $\Omega$ notation provides an **asymptotic lower bound**. For a given function $g(n)$, we denote $\Omega(g(n))$ the set of functions:
$$\begin{align*}
\Omega(g(n))=\{f(n)\mid \exists c &\gt 0\exists n_{0} \forall n\ge n_{0}: 0 \le cg(n) \le f(n)\}
\end{align*}$$
if $f(n)$ belongs to $\Omega(g(n))$, there exists positive constants $c$ and $n_{0}$ such that $f(n)$ is always greather than or equal to $cg(n)$ for sufficiently large $n$. 

Let's show that $4n^{2} + 100n + 500 = \Omega(n)$.
$$\begin{align*}
4n^{2}+100n+500 &\ge cn\\
4n+100+ \frac{500}{n} &\ge c
\end{align*}$$
This inequality holds when $n_{0}$ is any positive integer and $c=4$ *(or less)*.

## $\Theta$-Notation

We use $\Theta$-notation for **asymptotically *tight* bounds**. For a given function $g(n)$, we denote by $\Theta(g(n))$, the set of functions:
$$\begin{align*}
\Theta(g(n))=\{f(n): \exists [c_{1},c_{2},n_{0}]\gt 0: 0 \le c_{1}g(n) \le f(n) \le c_{2}g(n)\}
\end{align*}$$
For all values of $n$ at and to the right of $n_{0}$, the value of $f(n)$ lies at or above $c_{1}g(n)$ and at or below $c_{2}g(n)$, in other words, for all $n\ge n_{0}$, $f(n) = g(n)$ to within constant factors.

