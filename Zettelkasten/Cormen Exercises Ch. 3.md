---
tags: algorithms
---

*3.1-1* *Modify the lower-bound argument for insertion sort to handle input sizes that are
not necessarily a multiple of 3.*

The argument states that if the largest elements of the array appear in the first $\frac{n}{3}$ positions, they should end somewhere in the last $\frac{n}{3}$ positions $A[\frac{2n}{3}+1:n]$, each should me moved through the middle portion by $\frac{n}{3}$ iterations of the inner loop, each of these $\frac{n}{3}$ values must pass through at least $\frac{n}{3}$positions each, the running time is $\Omega(n^{2})$.

Generalizing for any multiple of a nonnegative integer $k$. Suppose that the array is divided into $\frac{n}{k}$ groups, and the largest elements are in the first $\frac{n}{k}$ positions $[1:\frac{n}{k}]$, they must end at the $\left[\frac{(k-1)n}{k}+1:n\right]$ portion of the array, by passing through each one of the $\frac{(k-2)n}{k}$ positions in the middle, each of the $\frac{n}{k}$ elements must pass through at least $\frac{(k-2)n}{k}$ positions. 