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