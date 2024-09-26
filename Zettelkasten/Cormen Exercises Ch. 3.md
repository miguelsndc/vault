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