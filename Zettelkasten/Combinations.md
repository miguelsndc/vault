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
This $2\times 1$ [[Matrix Definition|matrix]] represent a combination as well. To denote a combination of $r$ elements in $n$, we say **$n$ choose $r$**, that's the convention.
# Complement Identity:
$$\begin{align*}
C(n,r)=C(n,n-r)
\end{align*}$$
