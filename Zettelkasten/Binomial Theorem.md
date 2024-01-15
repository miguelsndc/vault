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
There's a bunch of useful identities related to the binomial theorem, we shall prove (almost) each one here.
>[!faq] Proposition
>Let $n$ be a nonnegative integer, then:
$$\sum_{k=0}^{n}{n\choose k}=2^{n}$$
>
# Proof
Using the binomial theorem with $x=1$ and $y=1$; we have:
$$\begin{align*}
2^{n}=(1+1)^{n}=\sum_{k=0}^{n}{n\choose k}1^{k}1^{n-k}=\sum_{k=0}^{n}{n\choose k}
\end{align*}$$
We can give a [[Combinatorial Proof]] for this too:
A set with $n$ elements has $2^n$ subsets, (see: [[Power Set]]), each with $0,1,2,\cdots,n$ elements, $n \choose 0$ counts the subsets with no elements, $n \choose 1$ counts those with one element, $n \choose 2$ those with two elements, $\cdots$, $n \choose n$ counts the whole set once. so:
$$\begin{align*}
\sum_{k=0}^{n}{n\choose k}
\end{align*}$$
Counts the number of subsets of a set with $n$ elements, so:
$$\begin{align*}
\sum_{k=0}^{n}{n\choose k} &= 2^{n}
\end{align*}$$
>[!faq] Proposition
>Let $n$ be a prositive integer, so: $$\sum_{k=0}^{n}(-1)^{k}{n \choose k} = 0$$
# Proof
Let's use $x=-1$ and $y=1$:
$$\begin{align*}
0 &=  0^{n}=(-1+1)^{n}\\
& = \sum_{k=0}^{n}{n \choose k}(-1)^{k}1^{n-k}{n\choose k}\\
&= \sum\limits_{k=0}^{n}(-1)^{k}{n\choose k}
\end{align*}
$$

>[!faq] Proposition
>Let $n$ be a nonegative integer, so: $$\sum\limits_{k=0}^{n}2^{k}{n \choose k}=3^{n}$$
# Proof:
Let's use $x=1$ and $y=2$:
$$\begin{align*}
3^{n}=(1+2)^{n}&= \sum\limits_{k=0}^{n}{n \choose k}2^{k}1^{n-k}\\
&= \sum\limits_{k=0}^{n}2^{k}{n\choose k}
\end{align*}$$
