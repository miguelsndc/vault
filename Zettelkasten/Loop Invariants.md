---
tags: algorithms
aliases: invariant, invariants
---
A Loop invariant is some predicate (condition) that holds true immediately before and immediately after each iteration of a loop. It has three properties:
- **Initialization**: It is true prior the first iteration of the loop
- **Maintenance**: If it is true before an iteration of the loop, it remains true before the next iteration.
- **Termination**: The loop terminates, and when it terminates, the invariant alongside the reason why the loop terminated usually gives us a useful property that helps show that underlying algorithm is correct.
See the example:

```c
int max(int n, int A[]) {
	int m = A[0];
	// m equals the greatest value in a[0..0] Initialization
	int i = 1;
	while (i != n) {
		// a equals the greatest value in a[0..]
		if (m < a[i])
	}
}
```

