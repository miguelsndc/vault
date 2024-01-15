---
tags: combinatorics
---
With [[Permutations]] we count the amount of $r$ subsets of a set with $n$ elements, with order in mind, meaning $\{a,b,c\} \ne \{b,a,c\}$. However, in a situation where order is *irrelevant*, permutations overcount.
Let $P(n,r) = \frac{n!}{(n-r)!}$ 
$P$ counts the number of $r$-permutations of $n$ elements. Observe that every $r$ set with $0 \le |r| \le |n|$ has exactly $r!$ permutations of it's own elements. We know $\frac{r!}{r!}= 1$, By dividing the $P$ by the number of permutations of $r$ we are considering every $r$ subset only once regardless of the orders. So the formula becomes:
$$\begin{align*}
C(n,r)=\frac{n!}{r!(n-r)!}
\end{align*}$$
This $C$ is called a **combination**. It counts the number of ways to **choose $r$ elements from $n$** elements. *(Note permutations count the number of ways to order $r$ elements in $n$)*. 

>[!faq] Question
>What's the number of ways to form a comittee of three people from a group of 12 ?

Note that $P(12,3)=\frac{12!}{(12-3)!}$ will count the number of $3$-ordered subsets from a group of $12$. A comittee of three people is formed by these three individuals regardless of the order they are chosen, by the way, order doesn't even matter at all in this case. We need *combinations* to do so, then:
$$\begin{align*}
C(12,3)&= \frac{12!}{3!(12-3)!}=220
\end{align*}$$
There's $220$ ways to form the comittee.
___
Combinations are so common in so many areas that there's a special notation for them:
$$\begin{align*}
C(n,r)&= {n\choose r}=\frac{n!}{r!(n-r!)}
\end{align*}$$
This $2\times 1$ [[Matrix Definition|matrix]] represent a [[Binomial Theorem|binomial]] coeffient, a special use case for combinations. A combination of $r$ elements in $n$, we say **$n$ choose $r$**, i mean that's what we are doing here, choosing $r$ subsets from $n$.
# Complement Identity:
Here we prove a important identity:
$$\begin{align*}
C(n,r)=C(n,n-r)
\end{align*}$$
**Combinatorial Proof**
Let $S$ be a [[Sets|set]] with $n$ elements. Let $r \in \mathbb{Z} \mid 0\le r \le n$. The number of ways to choose $r$ element [[Subsets]] from $S$ is ${n \choose r}$. However, each subset $A$ with $r$ elements can be defined by which elements **are not** in $A$, i.e $\overline{A}$. This means that **not choosing $n-r$ elements, equals choosing $r$ elements**.
**Algebraic Proof**:
$$\begin{align*}
C(n,r) &= \frac{n!}{r!(n-r)!}\\
C(n, n-r)&= \frac{n!}{(n-r)!(n-(n-r))!}\\
&= \frac{n!}{(n-r)!(n-n+r)!}\\
&= \frac{n!}{(n-r)!r!}\\
&= \frac{n!}{r!(n-r)!}\\
&= C(n,r)
\end{align*}$$
___
Permutations are combinations multiplied by the permutation of the $r$ [[Subsets]]. Since we divide a permutation by $r!$ to obtain the combinations, So relation is stablished below:
$$\begin{align*}
P(n,r)=C(n,r)\cdot P(r,r)
\end{align*}$$
From this we get all three operations:
$$\begin{align*}
P(n,r)&= C(n,r)\cdot P(r,r)\\
C(n,r)&= \frac{P(n,r)}{P(r,r)}\\\\
P(r,r)&= \frac{P(n,r)}{P(r,r)}
\end{align*}$$
