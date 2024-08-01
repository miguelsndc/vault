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