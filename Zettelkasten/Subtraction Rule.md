---
tags: combinatorics
---
>[!tip] Definition
The Subtraction rule says that if a task can be done in **either** $n_{1}$ or $n_{2}$ ways, then the total number of ways to do the task is $n_{1} + n_{2}$ minus the number of ways to do the task that were counted in **both** $n_{1}$ and $n_{2}$; 
## Example

>[!faq] Question
>How many bit strings of length $7$ **either** start with ""$1$"" bit or end with the $3$ "$000$" bits ?

Counting how many start with $1$: we have $1 \cdot 2 \cdot 2 \cdot 2 \cdot 2 \cdot 2 \cdot 2$ or $2^{6}$ ways.
Counting how many end with $000$: we have $2 \cdot 2 \cdot 2 \cdot 2 \cdot 1 \cdot 1 \cdot 1$, since we have only one option at the three last digits, which is $0$, so: $2^{4}$ ways.

notice that if we sum these two and leave it as it is, *we are counting the occurrences that go in both [[Sets|sets]] **twice***. so we got to subtract every set by the thing that happens in both, the string: $1 - 2 - 2 - 2- 1 - 1- 1$, so $2^{3}$, and then add this to the total, see:

Strings that start with one: $2^{6} = 64 - 2^{3} = 56$
Strings that end with three zeros: $2^{4}-2^{3}=8$ 
Strings that start with one **and** end with three zeros: $2^{3}=8$

So summing everything up we have: $56+8+8=72$.


