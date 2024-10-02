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
O(g(n))=\{f(n)\mid \exists c\exists n_{0} (\forall n\mid(n&\ge n_{0})\land 0 \le f(n) \le cg(n)\}
\end{align*}$$
A function $f(n)$ belongs to the set $O(g(n))$ if there exists a positive constant $c$ such  that $f(n)\le cg(n)$ for sufficiently large $n$ *(sufficiently large being $n \ge n_{0}$)*. 