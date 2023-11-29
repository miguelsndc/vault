---
tags: combinatorics
---
The product rule is a **pattern of thinking** used throughout combinatorics to represent the amount of all possible outcomes a procedure with **two or more tasks** can reach.

>[!Definition]
>If a procedure can be divided into two tasks (or more), the rule of product states that if task one consists of $n_{1}$ steps and task two of $n_{2}$ steps, then the procedure can be done in $n_{1}\cdot n_{2}$ steps.

It's possible to visualize this procedure in a tree-like style where each leaf maps to all elements of the other collection, representing all possibilities for t

In a problem when exclusion or allocation of some value to a reserved space is necessary, we **subtract** this value out of our product to ensure that its discarded in the other possibilities.