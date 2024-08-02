---
tags: algorithms
---
Insertion sort is an efficient algorithm for sorting a small number of elements, it works as someone might sort a hand of playing cards, you first start with an empty left hand and a pile of cards in the table, then, you remove the first card from the pile and put it in your left hand. Now you remove cards from the pile and **insert** them in the right position on your left hand, you start with the rightmost card and move left until you've found a card whose value is less than the card in your hand, so you place the card in your hand just to the right of this card in your left hand. At all times the cards in your left-hand are sorted. 

Here's a pseudocode:
```
procedure insertion_sort(A, n)
	for i = 2 to n
		key = A[i]
		// insert A[i] into the sorted subarray A[1:i-1]
		j = i - 1
		while j > 0 and A[j] > key
			A[j + 1] = A[j]
			j = j - 1
		A[j + 1] = key
```

The index $i$ indicates the "current card" being inserted into our hand, while the subarray $A[1:i-1]$ is our left hand, and $A[i+1:n]$ is what's left in the table, In fact, elements in $A[1:i-1]$ are the elements *originally* in that position but in sorted order. The algorithm works by moving elements already in $A[1:i-1]$ to the right until a position for $i$ is found.
These properties of $A[1:i-1]$ are the [[Loop Invariants]] of the algorithm, let's define it.

The loop [[Loop Invariants|invariant]]: *At the start of each iteration of the for loop on lines $2$-$9$, the subarray $A[1:i-1]$ consists of the elements originally in $A[1:i-1]$, but in sorted order*.
## (Informal) Proof of Correctness

Here we show the correctness of Insertion Sort through the loop invariant previously defined.
- **Initialization**: Here we show that the invariant holds before the first loop iteration, when $i = 2$. he subarray $A[1:i-1]$ consists of just the element $A[1]$, which is sorted.
- **Maintenance**: Showing that the loop maintains the invariant on each iteration. Informally, the body of the for loop works by moving elements $A[i-1], A[i-2], A[i-3]$ to the right until it finds a suited position for $A[i]$, so the subarray $A[1:i]$ consits of elements previously in $A[i]$ but in sorted order. Notice that after the iteration the $i$ increases, preserving the loop invariant.
- **Termination**: Finally, we examine the loop termination. The loop starts at $2$ and increases by $1$ every iteration, once $i$'s value exceed $n$, the loop terminates. That is, the loop terminates once $i=n+1$, substituting in the invariant yields the subarray $A[1:n]$, which is previously $A[1:n]$ but in sorted order, therefore the algorith **is correct**.

Please notice we also need a loop invariant for the *while* loop, and a more formal proof is more bullet-proof, this is a sketch.
___
# Analysis

Consider the conventions defined in the [[Running Time Conventions]] note.
Let $T(n)$ represent the time taken by insertion sort, Let also $t_{i}$ represent the time taken by the `while` loop.

```
procedure insertion_sort(A, n)
	for i = 2 to n
		key = A[i]
		// insert A[i] into the sorted subarray A[1:i-1]
		j = i - 1
		while j > 0 and A[j] > key
			A[j + 1] = A[j]
			j = j - 1
		A[j + 1] = key
```

| Line | Cost  | Executions                       | Total time                          |
| ---- | ----- | -------------------------------- | ----------------------------------- |
| 2    | $c_1$ | $n$                              | $c_{1}n$                            |
| 3    | $c_2$ | $n-1$                            | $c_2(n-1)$                          |
| 4    | $0$   | $0$                              | $0$                                 |
| 5    | $c_4$ | $n-1$                            | $c_3(n-1)$                          |
| 6    | $c5$  | $\sum\limits_{i=2}^{n}t_{i}$     | $c_5\sum\limits_{i=2}^{n}t_{i}$     |
| 7    | $c_6$ | $\sum\limits_{i=2}^{n}(t_{i}-1)$ | $c_6\sum\limits_{i=2}^{n}(t_{i}-1)$ |
| 8    | $c_7$ | $\sum\limits_{i=2}^{n}(t_{i}-1)$ | $c_7\sum\limits_{i=2}^{n}(t_{i}-1)$ |
| 9    | $c_8$ | $n-1$                            | $c_8(n-1)$                          |

So the total time is:
$T(n) = c_{1}n+c_{2}(n-1)+c_{3}(n-1)+c_{5}\sum\limits_{i=2}^{n}t_{i}+c_{6}\sum\limits_{i=2}^{n}(t_{i}-1)+c_{7}\sum\limits_{i=2}^{n}(t_{i} - 1)+c_{8}(n-1)$.
Even for inputs of a given size, the runnig time might depend on *which* input wa