---
tags: combinatorics
---
The complement rule for counting says that we don't really need to solve the problem directly, instead, we can answer the **opposite** problem. That means, *find all the outcomes where our condition isn't true*, then subtract from the [[Sample Space]], 

>[!tip] Technique Definition
>Suppose we want to find all $x$ outcomes in a sample space $z$. If finding $x$ feels to overwhelming, we can find all outcomes $y$ in $z$ where $x$ isn't true, and then subtract $y$ from $z$ to get the outcomes $x$.

## Example

>[!faq] Question
>If a student ID is made up of three uppercase letters and two numbers, what is the number of ID's that have some repetition ?

First, note that to find all cases where there's at least one repetition, we need to account the cases: *three letters, two letters, two numbers, two letters and two numbers, three letters and two numbers*.
Calculating all this feels like a big waste of time, instead, let's find our [[Sample Space]].
We know the alphabet has $26$ letters, so we have $26$ cases for each ID letter: $26 \cdot 25 $
