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
procedure LINEAR_SEARCH(A,n,x)
	index = NIL
	for i = 1 to n
		if A[index] == x
			index = i
	return index
```

Loop [[Loop Invariants|invariant]]: At the start of each iteration, the `index` variable contains the last index of occurrence of value $x$ or `NIL` otherwise.

> This fulfills the requirements of the question, however, it'd be more clever to break the loop once we fond the index, however i'll take advantage from this lack of information lol.

- **Initialization**: Before the first iteration, the `index` variable contains `NIL`, since we have scanned no subarray yet, we can say we scanned the empty subarray, and the empty subarray does not contain $x$, therefore initialization holds.
- **Maintenance**: At the start of every iteration we compare `A[index]` to `x`, If it is equal, then the `index` contains the last occurrence of `x` in the subarray $A[1:i]$, if it isn't, then `index` contains either `NIL` or the last occurrence of `x` in the subarray $A[1:i-1]$ of previous iteration, and after the iteration it contains the last occurrence of `x` in subarray $A[1:i-1]$, therefore maintaning invariance.
- **Termination**: After the last iteration, $i$ will be $n + 1$, and since the invariant is maintained,`index` will contain the last occurrence of `x` in the subarray $A[1:n]$, therefore the algorithm is correct.

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
