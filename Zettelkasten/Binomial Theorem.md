---
tags: binomial-theorem, combinatorics
aliases: binomial, binomial theorem
---
The Binomial Theorem is related to the expansion of [[Polynomials]] of the form $(x+y)^{n}$
with $n\in \mathbb{Z}^{+}$. 

> [!tip] Theorem
> Let $x$ and $y$ be variables, and let $n$ be a nonnegative integer, then: $$(x+y)^{n} = \sum_{j=0}^{n}{n\choose k} x^{n-j}y^{j}
= {n \choose 0}x^{n}+ {n\choose 1}x^{n-1}y+{n\choose 2}x^{n-2}y^{2}+\cdots+{n\choose n}y^{n}$$

Before giving a proof of this theorem, let's reason about the expansion of $(x+y)^{3}$. First, it can be written as $(x+y)(x+y)(x+y)$, and the powers of $x$'s and $y$'s will be: $x^{3},x^{2}y, xy^{2},y^{3}$. 
The only way to get $x^{3}$ is to choose $x$ in all three sums, or **not** choose $y$ in all three sums, both of which can happen only **once**, so the coefficient of $x^{3}$ is $1$.
To get $x^{2}y$, $x$ must be chosen twice from the sums, consequently, $y$ is chosen once. so there's ${3 \choose 2}$ or ${3 \choose 1}$, if you think in terms of the $x$'s and $y$'s, respectively, so the coefficient is $3$, similarly for $xy^{2}$. for $y^{3}$ there's only one way to do so. So the expansion of $(x+y)^{3}$ is $x^{3}+3x^{2}y+3xy^{2}+y^{3}$.
___
## Proof of the Binomial Theorem
Note that the terms of the expansion are of the form: $x^{n-j}y^{j}$ with $j=0,1,2,\cdots,n$. To find the number of terms for $x^{n-j}y^{j}$is necessary to choose $n-j$ terms (such that the other $j$ terms are the $y$'s), so the coefficient for $x^{n-j}y^{j}$ is ${n \choose n-j}$ which is equal to $n \choose j$.
____
We can calculate both entire expansions of binomials or calculate a specific coeficient in a expansion, see:
$\text{What is the coefficient of } x^{12}y^{13} \text{ in the expansion of } (x+y)^{25}$?
$$\begin{align*}
{25 \choose 13}1^{12}1^{13}&= \frac{25!}{13!12!}=5200030
\end{align*}$$
In this case we need to consider the signs and possible 