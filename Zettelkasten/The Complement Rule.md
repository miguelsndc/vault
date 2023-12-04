---
tags: combinatorics
---
The complement rule for counting says that we don't really need to solve the problem directly, instead, we can answer the **opposite** problem. That means, *find all the outcomes where our condition isn't true*, then subtract from the [[Sample Space]], 

>[!tip] Technique Definition
>Suppose we want to find all $x$ outcomes in a sample space $z$. If finding $x$ feels too overwhelming, we can find all outcomes $y$ in $z$ where $x$ isn't true, and then subtract $y$ from $z$ to get the outcomes $x$.
>
>When you see ***at least "something"***

## Example

>[!faq] Question
>If a student ID is made up of three uppercase letters and two numbers, what is the number of ID's that have some repetition ?

First, note that to find all cases where there's at least one repetition, we need to account the cases: *three letters, two letters, two numbers, two letters and two numbers, three letters and two numbers*

Calculating all this feels like a big waste of time, instead, let's find our [[Sample Space]] and work our way through the **complement rule**.
We know the alphabet has $26$ letters, so we have $26$ cases for each ID letter: $26 \cdot 26 \cdot 26$, same goes for the $10$ digits, two times.

So our sample space is $26\cdot26\cdot26\cdot10\cdot10 = 26^{3}\cdot 10^{2}$ possible ID's.
We know we need the cases where we have **at least one repetition**, so, we can find the cases where **there's no repetition at all, and subtract them from the total**, to obtain the cases where we'll have repetition.

For ID's with no repetition, we gotta decrease one every time we place a digit, because we can't repeat (no shit), so we have: $26\cdot25\cdot24\cdot10\cdot9$ ways.

So our big answer is: $26^{3}\cdot10^{2}-1404000$.