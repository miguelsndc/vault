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
- **Maintenance**: Before the iteration, 
