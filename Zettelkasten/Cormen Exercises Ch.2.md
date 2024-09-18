---
tags: algorithms
---
*2.1-1 Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on an array initially containing the sequence $[31; 41; 59; 26; 41; 58]$* 

Did on paper.

*2.1-2 Consider the procedure SUM-ARRAY on the facing page. It computes the sum of the $n$ numbers in array $A[1:n]$. State a loop invariant for this procedure, and use its initialization, maintenance, and termination properties to show that the SUM-ARRAY procedure returns the sum of the numbers in $A[1:n]$.*

```
procedure SUM-ARRAY(A,n)
	sum = 0
	for i = 1 to n
		sum = sum + A[i]
	return sum
```

Loop [[Loop Invariants|invariant]]: At the start of every iteration, the $\rm{sum}$ variable contains the sum of all elements in the subarray $A[1:i-1]$. 

- **Initialization**: Before the first iteration, the sum variable contains the sum of all elements in the subarray $A[1:0]$, which does not exist and therefore is empty, and the sum is $0$.
- **Maintenance**: On each iteration,  on the body we add sum to itself plus $A[i]$, denoting the sum of all elements from $A[1:i-1]$ and $A[i]$, therefore being the sum of the subarray $A[1:i]$, at the end $i$ increments and the sum corresponds to the sum of elements of $A[1:i-1]$, therefore preserving loop invariance.
- **Termination**: The loop runs from $1$ to $n$, and since the invariant states that sum holds the sum of elements in $A[1:i-1]$, when the loop ends, $i$ is $n+1$, and substituing that into the invariant, sum corresponds now to the sum of elements of $A[1:n]$, therefore the algorithm is correct.

*2.1-3 Rewrite the INSERTION-SORT procedure to sort into monotonically decreasing instead of monotonically increasing order.*

```
procedure INSERTION_SORT(A,n)
	for i = 2 to n
		key = A[i]
		j = i - 1
		while j > 0 and A[j] <= key
			A[j + 1] = A[j]
			j = j - 1
		A[j + 1] = key
```

*2.1-4 Write pseudocode for linear search, which scans through the array from beginning to end, looking for x. Using a loop invariant, prove that your algorithm is correct. Make sure that your loop invariant fulûlls the three necessary properties.*
```
procedure LINEAR_SEARCH(A, n)
```


*2.1-5*
```
procedure ADD-BINARY-INTEGERS(A,B,n)
	carry  = 0
	C[0:n] = 0 // filled with zeroes
	for i = 0 to n - 1
		C[i] = (A[i] xor B[i]) xor carry
		carry =(A[i] and B[i]) or (carry and (B[i] or A[i]))
	C[i] = carry
	return C
```

*2.2-1 Express the function $\frac{n^{3}}{1000}+100n^{2}-100n+3$ in terms of $\Theta$ notation.*

Let $F(n)$ be the function in the statement, notice that the leading coefficient of $F$ has degree $3$, which belongs to the order of $\Theta(n^{3})$, since:
$$\begin{align*}
\lim_{n\rightarrow\infty}\frac{F(n)}{n^{3}}&= \frac{\frac{n^{3}}{1000}+100n^{2}-100n+3}{n^{3}} \\
&= \lim_{n\rightarrow\infty} \frac{n^3(\frac{1}{1000} + 100 \frac{1}{n} - 100 \frac{1}{n^{2}} + 3 \frac{1}{n^{3}})}{n^{3}}\\
&= \lim_{n\rightarrow\infty} \frac{n^{3}}{n^{3}}=1
\end{align*}$$
Therefore $F(n) \in \Theta(n^{3})$.

$2.2-2$

```
procedure SELECTION-SORT(A,n)
	for i = 1 to n - 1
		small_i = i + 1
		for j = i + 1 to n
			if A[j] < A[small_i]
				small_i = j
		swap(A[i], A[small_i])
```

[[Loop Invariants]]: After each iteration, the subarray $A[1:i]$ is sorted.
Inner loop: After each iteration, `small_i` contains the index of the smallest element in the subarray $A[i+1:j]$.

- **Initialization**: For the inner loop, prior to the first iteration, $j$ contains $i + 1$, since $i=1$, `small_i` contains the smallest element of $A[i + 1: j]=A[2:2]$ which is $A[2]$ itself. Prior to the first iteration, $i=1$ and the subarray is $A[1:1]$ which is sorted.
- After the start of each iteration $j = i + 1$ up to $n$ and we scan the subarray $A[i+1:j]$ looking for the smallest element.  For the outer loop, once the inner loop finds the smallest element in $A[i+1:n]$ we swap it with $A[i]$, keeping the subarray $A[1:i]$ sorted.
- Once the inner finishes, we find the smallest element of subarray $A[i+1:n]$ which is the smallest of the unsorted part, since the outer loop goes only to $n - 1$, we find the smallest element in $A[n-1:n]$, and swap with $A[n-1]$, keeping the subarray $A[n-1:n]$ sorted, one the loop finishes, $A[1:n]$ is sorted.

It only needs to run $n-1$ times because the inner loop will scan through the remaining subarray, and swap the $n$ element with the $n - 1$ element if needed, if we went all the way up to $n$ in the outer loop, one iteration is wasted.

There's no difference between the best case and the worst case since there's no stopping condition in the inner loop, it'll always scan the entire subarray no matter what, keeping a time of, ignoring the inner lines constant execution time:
$$\begin{align*}
\sum\limits_{i=1}^{n-1}\sum\limits_{j=i+1}^{n}1&= \sum\limits_{i=1}^{n-1}n-(i+1)+1\\
&= \sum\limits_{i=1}^{n-1} n-i\\
&= \left(\sum\limits_{i=1}^{n}(n-i)\right)-(n-i)\\
\frac{(n-i)(n-i+1)}{2}-(n-i)\\
&\in \Theta(n^{2})
\end{align*}$$
*$2.2-3$ Consider linear search again (see Exercise 2.1-4). How many elements of the input array need to be checked on the average, assuming that the element being searched for is equally likely to be any element in the array? How about in the worst case? using $\Theta$ notation, give the average-case and worst-case running times of linear search. Justify your answers.*

Since the elements are equally likely to be selected, we can assume the probability of a element lying in a position "$i$" is given by a uniform distribution, and it should be somewhere in the average, since the average of a uniform distribution is given by: $\frac{1}{2}(a + b)$ where $a$ and $b$, in this context is the first and last index of the array, we can expect the element to be in the middle, and we need to check $\frac{n}{2}$ elements to get it.

In the worst case the element is at the last index, and we need to perform $n$ checks.

In the worst case, assuming that checking takes a constant time $c$:
$$\begin{align*}
\sum\limits_{i=1}^{n}c=c\sum\limits_{i=1}^{n}1=c(n-1+1)=cn \in \Theta(n)
\end{align*}$$
In the average case, we'd only need to loup through half the array. So with the same assumptions as before:
$$\begin{align*}
\sum\limits_{i=1}^\frac{n}{2}c=c\sum\limits_{i=1}^{\frac{n}{2}}1=
c\left(\frac{n}{2}-1+1\right)=\frac{cn}{2}\in  \Theta(n)

\end{align*}$$
*2.2-4 How can you modify any sorting algorithm to have a good best-case running time?*

In a world of rainbows and cats and ignoring all probabilities, we could naively check if the array is already sorted in $\Theta(n)$ time and only proceed otherwise. This way we'd have the ideal best case.