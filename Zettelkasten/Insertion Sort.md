---
tags: algorithms
---
Insertion sort is an efficient algorithm for sorting a small number of elements, it works as someone might sort a hand of playing cards, you first start with an empty left hand and a pile of cards in the table, then, you remove the first card from the pile and put it in your left hand. Now you remove cards from the pile and **insert** them in the right position on your left hand, you start with the rightmost card and move left until you've found a card whose value is less than the card in your hand, so you place the card in your hand just to the right of this card in your left hand. At all times the cards in your left-hand are sorted. Here's a pseudocode:
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
