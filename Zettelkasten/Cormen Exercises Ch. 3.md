---
tags: algorithms
---

*3.1-1* *Modify the lower-bound argument for insertion sort to handle input sizes that are
not necessarily a multiple of 3.*

The argument states that if the largest elements of the array appear in the first $\frac{n}{3}$ positions, they should end somewhere in the last $\frac{n}{3}$ positions $A[\frac{2n}{3}+1:n]$, each should me moved through the middle portion by $\frac{n}{3}$ iterations of the inner loop, each of these $\frac{n}{3}$ values must pass through at least $\frac{n}{3}$positions each, the running time is $\Omega(n^{2})$.

Generalizing for any multiple of a nonnegative integer $k$. Suppose that the array is divided into $\frac{n}{k}$ groups, and the largest elements are in the first $\frac{n}{k}$ positions $[1:\frac{n}{k}]$, they must end at the $\left[\frac{(k-1)n}{k}+1:n\right]$ portion of the array, by passing through each one of the $\frac{(k-2)n}{k}$ positions in the middle, each of the $\frac{n}{k}$ elements must pass through at least $\frac{(k-2)n}{k}$ positions.  the time taken by $\f{InsertionSort}$ in the worst-case is at least propotional to:
$$\begin{align*}
\frac{n}{k}\cdot \frac{n(k-2)}{k}&= \frac{n^{2}(k-2)}{k²} \in\Omega(n² )
\end{align*}$$
*3.1-2* *Using reasoning similar to what we used for insertion sort, analyze the running
time of the selection sort algorithm*

```
procedure SELECTION-SORT(A,n)
	for i = 1 to n - 1
		small_i = i
		for j = small_i + 1 to n
			if A[j] < A[small_i]
				small_i = j
		swap(A[i], A[small_i])
```

Selection sort works by repeatedly finding the smallest element in $[i+1:n]$ and placing it at the $i$ position every iteration, because the outer loop will run at least $n$ times, the running time is dominated by the inner loop, that will always pass through the entire $[i+1:n]$ subarray. Resulting in $\frac{n(n-1)}{2}$ iterations, which characterizes $O(n^{2})$. In fact the algorithm will always perform $\frac{n(n-1)}{2}$ iterations, there is no stopping or early quit conditions, regardless of the nature of the input, the algorithm will always perform the same number of iterations, which means it is in $\Omega(n^{2})$ too, and by consequence, in $\Theta(n^{2})$. It is highly predictable, deterministic i would say, in it's running time.

$3.1-3$ 
The answer is pretty much equal to $3.-1-1$, if you let $\frac{1}{k}= \alpha$. The value of $\alpha$ that maximizes the number of times that the $\alpha n$ values must go through the $1-2\alpha$ middle positions is $\alpha = \frac{1}{n}$, where each element is it's own group, it'd need to pass through $(1-2\alpha)n= (1 -\frac{2}{n})n =n-2$ positions which is the maximum possible. An additional restriction to $\alpha$ would be that it needs to divide $n$, but $\alpha= \frac{1}{n}$ already fulfills the requirement.  

$3.2-1$ $\max\{f(n),g(n)\}=\Theta(f(n)+g(n))$.

Recalling the definition of $\Theta$ notation, it means that the functions are bounded above and below by constant factors $c_{1}$ and $c_{2}$ when the input $n$ grows past some constant $n_{0}$. Therefore, here we need to figure out the upper and lower bounds for $\Theta(f(n) + g(n))$:
$$\begin{align*}
\max\{f(n),g(n)\} \in \Theta(f(n) + g(n)) \implies \max\{f(n)+g(n)\}\in O(f(n)+g(n))\land \\ \max\{f(n)+g(n)\} \in \Omega(f(n)+g(n))
\end{align*}$$
If it's bounded above by $O(h(n))$ and below by $\Omega(h(n))$, it is tightly bounded to $\Theta(h(n))$, so let's prove the cases, suppose $f(n)\ge g(n)$, the other case is proven by symmetry.
$$\begin{align*}
f(n) \in O(f(n)+g(n))
\implies f(n)&\le c(f(n)+g(n))\\
f(n)&\le cf(n)+cg(n)
\end{align*}$$
Choose any $c \ge 1$ and the equality is satisfied, given the assumption that $f(n)\ge g(n)$.

$$\begin{align*}
f(n) \in \Omega(f(n)+g(n))
\implies f(n)&\ge c(f(n)+g(n))\\
f(n)&\ge cf(n)+cg(n)
\end{align*}$$
Choose any $c \lt \frac{1}{2}$ and the equality is satisfied, given the assumption that $f(n)\ge g(n)$.

So for values $c_{1}=1$ and $c_{2}=\frac{1}{2}$, $\max\{f(n), g(n)\}=\Theta(f(n) + g(n))$ within constant factors $1$ and $\frac{1}{2}$:
$$\begin{align*}
\frac{1}{2}(f(n)+g(n)) &\le \max\{f(n),g(n)\} \le f(n)+g(n)  
\end{align*}$$
$3.2-2$ The statement is meaningless because $O$ notation describes and upper bound for a function, in this case, $O(n^{2})$ states that any function $f(n) = O(n^{2})$ is upper-bounded by some constant factor $c$ such that $f(n) \le c n^{2}$ for some $n \ge n_{0}$, saying that $A$'s running time is at least $O(n^{2})$ misuses $O$ notation for $\Omega$ notation, contradicting itself, lacking mathematical rigor, huge ambiguity and also being prone to misunderstandings and incorrect interpretations .

$3.2-3$ Yes, just choose $c \ge 2$ in the first and some big $c$ on the second for the respective $O(2^{n})$ definition and you're good to go, saying that it doesn't belong is the same as saying that $n+1 \notin O(n)$ or $2n \notin O(n)$.

$3.2-4$ **Prove that:** *For any two functions $f(n)$ and $g(n)$, we have $f(n) =\Theta(g(n))$ if and only if $f(n) = O(g(n))$ and $f(n) = \Omega(g(n))$.*

$(\rightarrow)$ Suppose $f(n)=\Theta(g(n))$, let's prove that $f(n)=O(g(n))$ and $f(n)=\Theta(g(n))$. By the definition of $\Theta$ notation, we have two constants $c_{1}$ and $c_{2}$ such that:
$$\begin{align*}
f(n)=\Theta(g(n)) \implies \exists c_{1}\exists c_{2}\mid 0\le c_{1}g(n)\le f(n) \le c_{2}g(n)
\end{align*}$$
Let's reexaminate the definitions of both $O$-notation and $\Omega$-notation:
$$\begin{align*}
f(n)=O(g(n)) \implies \exists c\mid 0\le f(n)\le cg(n)
\\
f(n)=\Omega(g(n)) \implies \exists c\mid 0\le cg(n)\le f(n)
\end{align*}$$
We can rewrite the definition of $\Theta$-notation as:
$$\begin{align*}
f(n) &= \Theta(g(n)) \implies \exists c_{1} \mid 0\le c_{1}g(n)\le f(n) \land\exists c_{2}\mid 0\le f(n) \le c_{2}g(n)\\
f(n)&= \Theta(g(n)) \implies f(n)=\Omega(g(n))\land f(n)=O(g(n))
\end{align*}$$
We can choose $c_{1}$ as constant for $\Omega$ and $c_{2}$ for $O$, and replace the statements with the respective asymptotic notations.

$(\leftarrow)$   Suppose $f(n)=O(g(n))$ and $f(n)=\Omega(g(n))$. Let's prove that $f(n)=\Theta(g(n))$. According to the definitions:
$$\begin{align*}
f(n)=O(g(n)) \implies \exists c\mid 0\le f(n)\le cg(n)
\\
f(n)=\Omega(g(n)) \implies \exists c\mid 0\le cg(n)\le f(n)
\end{align*}$$
Let $c_{1}$ be the constant bounding $f(n)$ from below and $c_{2}$ bounding $f(n)$ from above, ($\Omega$ and $O$, respectively):
$$\begin{align*}
f(n)=O(g(n)) \implies  0\le f(n)\le c_{2}g(n)
\\
f(n)=\Omega(g(n)) \implies  0\le c_{1}g(n)\le f(n)
\end{align*}$$
We can rewrite this as:
$$\begin{align*}
0\le c_{1}g(n)\le f(n) \le c_{2}g(n)
\end{align*}$$
and preserve the meaning of the predicate, as seen before, this is the definition of the $\Theta$ notation, therefore $f(n)=\Theta(g(n))$.

Hence the theorem is proven $(\iff)$.

$3.2-5$ Prove that the running time of an algorithm is $\Theta (g(n))$ if and only if it's worst-case running time is $O(g(n))$ and it's best-case running time os $\Omega(g(n))$

$(\rightarrow)$ Suppose the running time of an algorithm is $\Theta(g(n))$, let's prove that it's worst-case time is $O(g(n))$ and best-case time is $\Omega(g(n))$. 

As we've proved above, $f(n)=\Theta(g(n)) \iff f(n)=O(g(n)) \land f(n)=\Omega(g(n))$. Since the algorithm is bounded above and below by $g(n)$ within constant factors, we can say that the worst-case is bounded from above by some constant $c_{2}$ which implies that the worst case is $O(g(n))$, and similarlly, the best-case is bounded from below by some constant $c_{1}$, which implies that the best-case is in $\Omega(g(n))$.

$(\leftarrow)$ Suppose an algorithms best-case running time is in $\Omega(g(n))$ and it's worst-case is in $O(g(n))$, let's prove that the algorithm runs in $\Theta(g(n))$.

Given the assumptions above, the algorithm's the worst-case is bounded from above and the best-case is bounded from below within constant factors of $g(n)$, By the theorem proven in $3.2-4$, this implies that the algorithm is in $\Theta(g(n))$, meaning that it always runs in some constant factor of $g(n)$.

The proposition is proven $(\iff)$.

$3.2-6$ Prove that $o(g(n)) \cap \omega(g(n))$ is the [[Empty Set]].

Given the definitions of [[Asymptotic Notation|little-oh]] and [[Asymptotic Notation|little-omega]], let's expand the expression:

$$\begin{align*}
o(g(n))\cap\omega(g(n))&= 
\{f(n) \mid 0 \le f(n) \lt cg(n) \} \cap \{ f(n) \mid 0 \le cg(n) \lt f(n)\}
\end{align*}$$
The intersection between the set of functions strictly greater than $g(n)$ and the set of functions strictly less than $g(n)$ asymptotically speaking, is the empty set.

$3.2-7$ Extend the asymptotic notations to work on functions of two variables that grow independently, $O$ is given, define $\Omega(f(n,m))$ and $\Theta(f(n,m))$.

$\Omega(f(n,m))$ $:=$ $\{ g(n,m):\text{ there exists constants } c, n_{0}, m_{0} \text{ such that } 0 \le cg(n,m)\le f(n,m) \text{ for all } n \gt n_{0} \lor m \gt m_{0}$     

$\Theta(f(n,m))$ $:=$ $\{ g(n,m):\text{ there exists constants } c_{1},c_{2}, n_{0}, m_{0} \text{ such that } c_{1}f(n,m) \le f(n,m) \le c_{2}g(n,m) \text{ for all } n \gt n_{0} \lor m \gt m_{0}$     
$3.3-1$ Show that if $f(n)$ and $g(n)$ are **monotonically increasing functions**, then so are functions $f(n) + g(n)$ and $f(g(n))$ and if $f(n) * g(n)$ are in addition nonnegative, then $f(n) \cdot g(n)$ is monotonically increasing.
$1)$ Recall that if a function $h$ is monotonically increasing, then for $n \le m$, $f(n) \le f(m)$. for both $n,m \in D_{h}$. We have both facts:
$$\begin{align*}
\begin{cases}
f(n)\le f(m) \;\;\forall n\le m\\
g(n)\le g(m) \;\;\forall n\le m
\end{cases}
\end{align*}$$
As long as both functions are defined in the same interval and have the same domain, we can confidently sum the inequalities above and obtain:
$$\begin{align*}
f(n)+g(n)&\le f(m)+g(n)\;\;\forall n\le m
\end{align*}$$
$2)$ Notice that we assume $f$ and $g$ the be monotonically increasing, that means that for $n\le m \implies g(n) \le g(m)$. Thus if we let $u=g(n)$ and $v = g(m)$, we can confidently say that $f(u) \le f(v)$ for $u\le v$, since $g$ is monotonically increasing. Therefore $f(g(n))$ is also a monotonically increasing function.

$3)$ Ill assume that $f(n)$ and $g(n)$ are both nonnegative, i didnt quite grasp what "in addition nonnegative" means.

Since $f(n) \ge g(n) \ge 0$  for all $n$, then multiplication won't change the sign of the results. whatever's positive remains positive.

Therefore the inequalities are preserved on multiplication and we can multiply them to obtain:
$$\begin{align*}
f(n)\cdot g(n)&\le f(m) \cdot g(n)\;\;\forall n\le m
\end{align*}$$
$3.3-2$) *Prove that $\floor{\alpha n} + \ceil{(1-\alpha)n}=n$ for any integer $n$ and for any real number $\alpha$  in the range $0\le \alpha \le 1$.*

Oh the good old linear interpolation, how beautiful is it ?

Let $f_{x} = \alpha n - \floor{\alpha n}$ and $f_{y}=(1-\alpha) n - \floor{(1-\alpha)n}$. So $f_x$ and $f_{y}$ are the decimal parts of $\alpha n$ and $(1-\alpha)n$.

Now let's rewrite $\alpha n$ and $(1-\alpha)n$ as:
$$\begin{align*}
\alpha n&= \floor{\alpha n} + f_{x}\\
(1-\alpha)n&= \floor{(1-\alpha)n} + f_{y} 
\end{align*}$$
Sum them up:
$$\begin{align*}
\alpha n + (1-\alpha)n&= \floor{\alpha n}+ \floor{(1-\alpha)n}+(f_{x}+f_{y})
\end{align*}$$
Notice that $f_{x}+f_{y} = 1$ because since $\alpha + (1-\alpha)=1$, any value that $\alpha$ multiplies and has decimal part $f_{x}$, multiplying $(1-\alpha)$ will get the complementary to sum $1$.

$$\begin{align*}
\alpha n + (1-\alpha)n&= \floor{\alpha n}+ \floor{(1-\alpha)n}+1\\
n= \alpha n + (1-\alpha)n&= \floor{\alpha n}+ \ceil{(1-\alpha)n}
\end{align*}$$
$\floor{x}+1=\ceil{x}$ whenever $x$ isn't an integer, this also works when $\alpha =1$ or $\alpha=0$, because:
$$\begin{align*}
\alpha=1 \implies \floor{1\cdot n} + \ceil{(1-1)n}=\floor{n}=n\\
\alpha=0 \implies \floor{0\cdot n}+\ceil{(1-0)n}=\ceil{n}=n
\end{align*}$$
___
$3.3-3$ Show that $(n+o(n))^{k}=\Theta(n^{k})$.

By the [[Binomial Theorem]]:

$$\begin{align*}
(n+o(n))^{k}=\sum\limits_{i=0}^{k} {n\choose i}n^{k-i}o(n)^{i}={n\choose 0}n^{k}+\cdots+ {n\choose n}o(n)^{k}
\end{align*}$$
The dominant factor here is the $n^{k}$, since $o(n)$ represents functions asymptotically non-tight to $n$. Therefore it is polynomially tightly bounded.

The floor and ceiling stuff is just straight up bullshit.

$3.3-4$

1) I don't fuck with logarithms.
2) $3.26)$   $n! = o(n^{n})$: This is true for all $n\gt 1$. $n!$ will always be strictly less than $n^{n}$ because both have $n$ terms, but $n! = n(n-1)(n-2)\cdots1$ and $n^{n}=n\cdot n \cdots n$ and for all the other $n-1$ terms, $n> (n-i),i=1,2,\cdots,n$.
3) $3.26)n! = \omega (2^{n})$. This is true for all $n\gt 3$,  

