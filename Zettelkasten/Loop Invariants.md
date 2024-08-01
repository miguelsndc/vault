---
tags: algorithms
aliases: invariant, invariants
---
A Loop invariant is some predicate (condition) that holds true immediately before and immediately after each iteration of a loop. It has three properties:
- **Initialization**: It is true prior the first iteration of the loop
- **Maintenance**: If it is true before an iteration of the loop, it remains true before the next iteration.
- **Termination**: The loop terminates, and when it terminates, the invariant alongside the reason why the loop terminated usually gives us a useful property that helps show that underlying algorithm is correct.
A loop invariant proof is a form of mathematical **induction**, the initialization being the base case, the maintenance the inductive hypothesis and the termination is where we show that our thesis holds (or not).

See an example:

```
procedure max(A[1..n], n)
	m <- A[1] 
	m is the greatest element in A[1..1]
	i <- 1
	while (i != n)
		m is the greatest element in A[1..i] 
		if (m < A[i]) m <- a[i]
		m is the greatest element in a[0..i+1]
		i <- i + 1
		m is the greatest element in a[0..i]
	loop terminated with m being the greatest element in a[1..i] and 
	since i == n, m is the greatest in a[1..n] hence the greatest in a
 ```
 
Here we can see every stage very clearly, each stage holds true, since the greatest element in a unitary array is just the element itself, initialization holds
During the loop, the comments in lines $6$ and $10$ show that the condition remains true before and after the iteration
And the termination shows that $m$ is the greatest in $a$.