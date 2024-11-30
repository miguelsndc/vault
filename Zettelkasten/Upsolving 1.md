---
tags: maratona
---

## M - Mahmound and the Triangle

[Link](https://vjudge.net/problem/CodeForces-766B/origin)

Sort the array and check on a $3$-window for triangle inequality between the two smallest and the largest one, like: $a[i-2]+a[i-1] > a[i]$ then we have a triangle.

## A - [Rudolph and the Christmas Tree](https://vjudge.net/problem/CodeForces-1846D)

We need a big floating point precision, using `long double` solves the issue, also setting a specific precision also does help. Using triangle similarity to figure out the smaller side of the trapezoid

## D - Counting L's

## F -  [Enough Array](https://vjudge.net/problem/AtCoder-abc130_d)

**Two Pointers**, beginning and end, keep a window of subarrays and subtract the beginning and add the end when sliding, keep this window sliding until end is reached by the two pointers, when a valid subarray is found sliding right, then all subarrays to the right of it are valid answers, so ´n - r + 1´ more subarrays are counted.
## K - [Election Quick Report](https://vjudge.net/problem/AtCoder-abc329_d)

Keep a variable holding the current winner, then compare it to the recently voted candidate, the smallest candidate with the most votes wins, no need for heaps and shi.

If candidates are equal pick the smallest index.

## L - [Trailing Zeros](https://vjudge.net/problem/CSES-1618)

Consider the prime factorization of a number, we know that a trailing 0 is formed by a multiplication between $2$ and $5$, we want the minimum between the powers of $2$ and $5$, since the $2$'s appear much more frequently in any number than the $5$'s, we really just need to know how many factors of $5$ exist. We just keep dividing by $\lceil{n/5}\rceil$ while $n$ is greather than $5$.