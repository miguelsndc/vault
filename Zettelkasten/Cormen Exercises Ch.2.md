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
Input: A list of integers A[1:n], a target `n`
Outputs: the index i of the first occurence of `n` in the list. NIL otherwise.
procedure LINEAR_SEARCH(A, n):
	for i = 1 to n
		if A[i] == n
			return i
	return NIL
```

**Loop invariant**: *At the start of each iteration, the subarray `A[1:i-1]`  does not contain the target `n` ,  

- **Initialization:** *(True before the first iteration):* The empty subarray of $A$ does not contain any element, thus not containing `n` as well.
- **Maintainence:** Prior to the iteration `i`, let's split into cases
	- If `A[i]` equals `n`, then the procedure terminates, and the subarray `A[1:i-1]` , in fact, does not contain `n`.
	- If `A[i]` does not equal `n` from the prior iteration, the subarray `A[1:i-1]` won't contain `n`, once the condition is checked false, the subarray `A[1:i]` won't contain `n`, once the loop skips to the next iteration, `i` increments by $1$, hence making the subarray `A[1:i-1]` not contain `n`, and the invariant remains true.
- **Termination:** Once the last iteration occurs, the subarray `i` equals `n+1`, and substituting into the subarray formula,$A[1:i-1]= A[1:n+1-1]=A[1:n]$, the entire array does not contain `n`, hence the invariant holds and we return NIL instead.
   
 
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
		for j = small_i + 1 to n
			if A[j] < A[small_i]
				small_i = j
		swap(A[i], A[small_i])
```

**Loop Invariant**: *The subarray `A[1:i]` contains the smallest elements of `A[1:n-1]` in ascending (sorted) order*.

- **Initialization**: *(Holds true prior the first iteration)* Prior to the iteration, the subarray `A[1:i]` is empty, therefore is trivially sorted.
- **Maintainance:** Assume the invariant holds for iterations up to `k`, Let's show it holds for `k + 1`;  We start by finding the smallest element in the subarray `A[k+1:n]`, let's say it's at index `u`. Then it's swapped with `A[k+1]`, and the subarray `A[1:k+1]` is sorted. Once `i` increments, the subarray `A[1:k]` is now sorted, containing the $k$ smallest elements of `A`, so the invariant holds.
- **Termination**: Once the last iteration is finished, by substituting terms, `i = n`, therefore the array `A[1:n-1]` contains the `n-1` smallest elements of `A` in ascending order.
Therefore, since `A[1:n-1]` contains all the `n-1` smallest elements in ascending order, the `n`th position contains the greatest element in `A` trivially, so the array is indeed sorted and the algorithm is correct.


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
___
## 2.3

*2.3.-1* *Using Figure 2.4 as a model, illustrate the operation of merge sort on an array initially containing the sequence $<3; 41; 52; 26; 38; 57; 9; 49 >$*

Did on paper.

$2.3-2$ *The test in line 1 of the $MergeSort$ procedure reads $\f{if}\,\, p\ge r$ rather than $\f{if}\,\,p \ne r$ .= If $MergeSort$ is called with $p\gt r$ then the subarray $A[p:r]$ is empty.
Argue that as long as the initial call of $MergeSort(A,1,n)$ has $n\ge 1$, the test
$\f{if}\,\, p \ne r$ suffices to ensure that no recursive call has $p\gt 0$.*

$p$ is the lower-bound and $r$ is the upper bound of the subarray $A[p:r]$. Notice that when we calculate $q = \lfloor (p + r) / 2 \rfloor$, we calculate the average between $p$ and $r$. The average of two numbers won't ever be smaller than the smallest number and neither greater than the greatest number, the smallest (and greatest) that an average can be is when both numbers are equal, i.e $p=r$.
As we go down in the recursion tree we get $p$ closer to $r$ more and more, and it bottoms out when they're equal, because, as i said, that's the greatest an average can be.
That's why checking for $p \ne r$ suffices as long as $n \ge 1$, if you call with $n \lt 0$ then $p \gt r$ and we are triying to sort an empty array. 

$2.3-2$ *State a [[Loop Invariants]] for the while loop of lines $12-18$ of the $Merge$ procedure. Show how to use it, along with the while loops of lines $20-23$ and $24-27$, to prove that the $Merge$ procedure is correct.*

```
// lines 12-18
while i < NL and j < NR
	if L[i] <= R[j]
		A[k] = L[i]
		i = i + 1
	else
		A[k] = R[j]
		j = j + 1
	k = k + 1
```

**Loop Invariant**: The subarray $A[p:k-1]$ contains the smallest elements of either $L[0:i-1]$ and $R[0:j-1]$ at each position, in sorted order.

**Initialization**: prior to the first iteration, $i=0,j=0$, both $L[0:i-1]$ and $R[0:j-1]$ are empty, and so is $A[p:k-1]$, therefore, trivially it contains the sorted smallest elements.
**Maintainance**: Assume the invariant holds true for $A[p:k']$  ($L[0:i'],R[0:j']$), let us show that is remains true for $k'+1$. 
- Assume line $13$ evaluates true
		Therefore, $L[i'] \le R[j']$, so we take $L[i']$ to fill position $A[k']$, and advance $i$ by 1. (Note that if both are equal, we can take whatever, but to avoid a redundant if-check, we condense both cases into one if).
- Line $13$ evaluates false
	- In this case, $R[j'] \lt L[i']$. Therefore we choose $R[j']$ to occupy position $A[k']$, as it is the smallest of the two.
At the end of both conditions we increment $k'$ by $1$, advancing $k$, therefore, $A[p:k+1]$ is sorted, containing the smallest of $L$ and $R$ at each position, so the invariant remains true.
**Termination** at the end of the condition, either $L$ or $R$ was exhausted, and $A[p:k]$ contains the sorted elements of all $L$ or (exclusive) all $R$.

So we are left to fill the remaining spaces with what's left of either $L$ or $R$:

```
// line 20-23
while i < NL
	A[k] = L[i]
	i = i + 1
	k = k + 1
// line 24- 27
while j < NR
	A[k] = R[j]
	j = j + 1
	k = k + 1
```

*Disclaimer: the cases are symmetric, i'll prove for $L/i$, and the same works for $R/j$.*

**Loop invariant(s)**: Let $u = k$ and $v=i$ before the first iteration, ($k$ and $i$ will increment and $u$ and $v$. will stay the same) The subarray $A[u:k-1]$ contains all the elements of $L[v:i-1]$.

**Initialization**:  The subarrays $A[k:k-1]$ and $L[i:i-1]$ are both empty, therefore, by definition, we can say they contain each other.
**Maintainance**: Assume as hypothesis that the invariant holds true for $k'$ and $i'$, let us show it remains true for $k'+1$ and $i'+1$.
After each loop the contents of $L[i']$ are copied to $A[k']$, and both are incremented by one, since $L$ is sorted, the subarray $A[u:k'+1]$ contains the elements of $L[v:i'+1]$, so the invariant remains true.
**Termination** at the end, the array $A[p:r]$ is sorted, and the proof also works for $j$ by symmetry, therefore the algorithm is correct.

$2.3-4$ *Use mathematical induction to show that when $n\ge 2$ is an exact power of $2$, the solution of the recurrence
$$\begin{align*}
T(n)=\begin{cases}
2 & \f{if}\,\, n = 2,\\
2T\left(\frac{n}{2}\right)+ n \,\, &\f{if} \,\, n>2
\end{cases}
\end{align*}$$
is $T(n) = n \log n$*

**Base case**: For $n = 2$, $T(n)$ evaluates to $2$, which is equal to $2 \log_{2}(2)=2\cdot1 = 2$. Therefore the base case holds
**Indutive Hypothesis**: Assume that $T(k)=k \log k$ when $k$ is a power of two.
**Thesis**: Let us show it holds for $k'=2*k$ *(aka the next power of two)*:
$$\begin{align*}
T(k')&= 2T(\frac{k'}{2})+k'\\
&= 2T(\frac{2\cdot k}{2})+k'\\
&= 2T(k)+k'\\
&= 2(k \log k)+k'\\
&= k'\log k+k'\\
&= k' \log (\frac{k'}{2})+k'\\
&= k' (\log(k')-\log(2))+k'\\
&= k'\log(k')-k'+k'\\
&= k'\log(k')
\end{align*}$$Therefore, by the inductive hypothesis, $T(k') =k'\log k'$. Therefore the statement is true for all $n$ power of $2$.

```
procedure RecursiveInsertionSort(A, p, r)
	if p > r
		RecursiveInsertionSort(A, p, r - 1)
	else
		key = A[r]
		j = r - 1
		while j > 0 and A[j] > key
			A[j + 1] = A[j]
			j = j - 1
		A[j + 1] = key
	
```

$$\begin{align*}
T(n)=\begin{cases}
c_{1} &\f{if}\,\, n \le 1\\
T(n-1) + n &\f{otherwise}
\end{cases}
\end{align*}$$
Which goes all the way to $O(n^{2})$  

*$2.3-6$*

```
procedure BinarySearch (A, p, r, target)
	q = (p + r) / 2
	if A[q] == target
		return q
	else if A[q] < target
		BinarySearch(A, q + 1, r, target)
	else
		BinarySearch(A, p, q, target)
	return NIL
```

The recurrence will look something like:
$$\begin{align*}
T(n) &= \begin{cases}
1 &\f{if}\,\, n = 1,\\
T\left(\frac{n}{2}\right) + 1 &\f{otherwise}
\end{cases}
\end{align*}$$
Which splits the problem in half on every recursion call, and since the inner procedure takes constant time, the time is $O(\log n)$ overall $T(n) = \log n + 1$. This also can be shown by induction when $n$ is a power of $2$:
**Base case**:  $n=2$ the cost is $T(\frac{2}{2})+1$ = $T(1) + 1= 1+1 = 2$ which is constant, $\log(2) = 1 + 1=\log2 +1$. 
**Hypothesis**: assume it works for $k$, $T(k) = \log k +1$
**Thesis**: lets show it works of $k' = 2\cdot k$
$$\begin{align*}
T(k')&=T(\frac{k'}{2})+1\\
&= T(\frac{2k}{2})+1\\
&= \log k+1+1\\
&= \log \frac{k'}{2}+1+1\\
&= \log k' - \log2 + 1+1\\
&= \log k' -1  + 1 +1\\
&= \log k' +1
\end{align*}$$
proof is complete, so $\f{BinarySearch}\in O(\lg n)$.

*2.3-6*

A rough idea of the algorithm is: use binary search on the elements already "inserted" back into the left portion of the array (the sorted elements). The original insertion sort looks for the correct position and shifts the elements up at the same time, with binary search we search faster but still need to shift the other elements up anyway, so the worst case is still $O(n^{2})$.

*2.3-8*

```
procedure TwoSum(S[1:n], x):
	i = 0
	j = n
	sort(S) // O(n lg n) auxiliary
	// O(n) main procedure
	while i < j
		if S[i] + S[j] == x
			return true
		else if S[i] + S[j] > x
			j--
		else
			i++
	return false
```

## Chapter Problems

*2-1* 

- *Show that insertion sort can sort $\frac{n}{k}$ sublists of length $k$ in $O(nk)$ worst-case runtime*
Given that insertion sort will run in $O(n^{2})$, the running time for sorting **all** $\frac{n}{k}$ sublists is given by:
$$\begin{align*}
O(\frac{n}{k}\cdot(k² ))
= O(nk)
\end{align*}$$
Where $\frac{n}{k}$ is the amount of lists and $k^{2}$, being $k$ the size o those lists, is the time the algorithm takes to sort each individual list.

- *Show how to merge the sublists in $O(n \log (\frac{n}{k}))$* worst-case time.

Given that we have $\lg(\frac{n}{k})$ times each with size $k$, the merge procedure can only be applied to pairs of lists, we can only merge two lists at a time, so each level in the merge tree takes $O(n)$ to merge, since there's $n$ items at each level, however we half the number of sublists and double their size, and it takes $\log (\frac{n}{k})$ time to get to a single list of size $n$, therefore the worst-case runtime is $O(n \log (\frac{n}{k}))$. Being more concise, at each level of the tree takes $O(n)$ time to merge all pairs of sublists, and takes $\log(\frac{n}{k})$ time to walk back to the root of the tree, outputting a time of $O(n \log \frac{n}{k})$

- *2-1 c)* We want a value of $k$ such that $O\left(nk + n\log\left(\frac{n}{k}\right)\right)= O(n \log n)$, (not exactly equal, but belong to the same order of growth). We want $k$ as a function of $n$, notice that for $k = \log n$, we have:
$$\begin{align*}
O\left(n\log n + n\log\left(\frac{n}{\log(n)}\right)\right)
\end{align*}$$
Since $n\log  n$ grows much faster than $n\log \frac{n}{\log{n}}$, the first term dominates the expression, thus both have (roughly) the same running time.

- We want to choose $k$ such that the modified algorithm has always a smaller runtime than the original merge-sort. We need to keep in mind that the underlying insertion sort will not work for too large lists, we need a reasonable splitting.

- *2-1 d)*  I could not stablish perfectly $k$ as a function of $n$ such that the size is the most optimal, however google says that for lists of $10-20$ elements is where insertion sort does it's business the best. so $k$ should be some value that splits everything into batches of $10-20$. assuming $10$:
$$\begin{align*}
k=\frac{n}{10}
\end{align*}$$
*2-2 Correctness of bubblesort*

```
procedure BubbleSort(A,n)
	for i = 1 to n - 1
		for j = n down to i + 1
			if A[j] < A[j-1]
				exchange A[j] and A[j - 1]

```

*A)* i'll need to say that one needs to stablish two loop invariants for the inner and the outer loop and then conclude by induction that the algorithm is correct.

$b)$ **Loop Invariant**: The element at the index $A[j]$ will contain the smallest element in subarray $A[j:n]$.
- **Initialization**: Prior to the first iteration, $j$ is equal to $n$, so the subarray is $A[n:n]$ which consists of a single element, therefore $A[j]$ contains the smallest element in that portion of the array (the only one).
- **Maintainance**: Assume the invariant holds for $j=k$, let's show it holds for $j'=k-1$. After each iteration, if the element at $A[j]$ is less than the element at $A[j']$, then they're swapped, at this point $A[j'] < j$, but when $j$ decrements itself, the value at index $j$ will be the smallest, hence the invariant holds, if it's not then $j$ is simply decremented now assuming the smallest value.
- **Termination**: From the rules above we infer that at the end of the loop, $j=i$, so  the smallest element at $A[i+1:j]$ is bubbled down to it's correct sorted position accompanied by $j$ doing the hard work.
*c)* **Loop invariant**: The subarray $A[1:i]$ is sorted.
- **Initialization**: At the start of the first iteration $i=1$, so the subarray $A[1:i]=A[1:1]$ which contains just a single element therefore it's sorted by definition
- **Mantainance:** Assume the invariant holds for $i = k$, let's show it holds for $i=k+1$. At the end of the inner loop, from the other invariant stated above, the position $A[j]$ is the smallest element at the subarray $A[j:n]$, at the end of that iteration, $j=i$, therefore, by the hypothesis the subarray $A[1:k]$ is sorted, since $k+1$ now contains an element in it's correct sorted position, the subarray $A[1:k+1]=A[1:i]$ is sorted. So the invariant holds
- **Termination**: At the end of the last iteration $i=n$, so the subarray $A[1:i]=A[1:n]$ is sorted, so the algorithm is correct. 
*d)* The running time of bubble sort is always $O(n^{2})$ regardless of best/worst case, because the algorithm needs to go through each element in the subarray $A[i+1:j]$ at every iteration. Insertion sort and bubble sort have the same worst case complexity, but insertion sort might do less swapping as less comparisons, and also has a better best case scenario.

___

```
procedure HORNER(A, n, x)
	p = 0
	for i = n down to 0
		p = A[i] + x * p
	return p
```
$A= [1,2,3]$ $n = 3$ $x=  2$; evaluate$P(x) = 1 + 2x+ 3x^{2}$ at $x = 2$.
- $p = 0$
- $p = A[3] + 2 * 0=A[3]$; $p = 3$
- $p = A[2] + 2 * 3 = 2 + 6 = 8$
- $p = A[1] + 2 * 8 = 1 + 16 = 17$
- $p = 17$
- $P(2) = 1 + 4+3*4=17$
Parenthesization: $1 + x(2+3x)$ from inside-out.
- $a)$ Complexity is $O(n)$ where $n$ is the number of coefficients in the polynomial.

- $b)$
```
procedure NaivePolynomial(A, n, x)
	p = 0
	for i = 0 to n
		k = 0
		for j = 0 to i
			k += A[i]
		p += k
```

Complexity of $O(n^{2})$, $Horner$ is two orders of magnitude faster than the naive implementation.

$c)$ **Loop invariant:** At the start of each iteration, $p = \sum\limits_{k=0}^{n-(i+1)} A[k+i+1]\cdot x^{k}$.
- **Initialization**: Prior to the first iteration, $p=\sum\limits_{k=0}^{n-n-1}A[k+i+1]\cdot x^{k} =0$.
- **Maintenance:** Let's assume as hypothesis