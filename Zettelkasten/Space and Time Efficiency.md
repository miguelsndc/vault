---
tags: algorithms
---
Time efficiency or time *complexity* indicates how fast an algorithm runs.
Space efficiency or space *complexity* refers to the amount of memory units required by the algorithm **in addition** to the space needed for it's output and input.

## Units for measuring running time
Counting an algorithm running time on seconds is prone to failure, since execution time in seconds or any unit of time is prone to external factors like: speed of the computer, the quality of the program written, the compiler used to generate machine code, and the difficulty of clocking the actual running time of the algorithm.
Also counting each operation the algorithm does is a *excessivily difficult task* and usually unnecessary. The thing to do is to count how many times the **basic operation** of the algorithm runs. The basic operation is *usually* the most time-consuming task in the algorithm's innermost loop.

## The analysis framework

The usual analysis framework is run by counting how many times the basic operation of the algorithm runs on inputs of size $n$. For example, let $c_{op}$ be the execution time of an algorithm's basic operation on a particular computer, and let $C(n)$ be the number of times this operation needs to be executed for this algorithm. Then we can estimate the running time $T(n)$ with:
$$\begin{align*}
T(n) &\approx c_{op}C(n)
\end{align*}$$
This formula should be used with caution, since $c_{op}$ is an approximation whose reliability is not always easy to assess, and $C(n)$ is also an approximation that **does not contain operations that are not basic**. However, using this approach, questions like *"How much longer the algorithm will take to run if we double it's input size ? ""*, Assuming $C(n) = \frac{1}{2}n(n-1)$, and for all but very small values of n:
$$\begin{align*}
C(n) &= \frac{1}{2}n(n-1) =\frac{1}{2}n^{2} - \frac{1}{2}n\approx \frac{1}{2}n^{2}\\
\frac{T(2n)}{T(n)}&=\frac{\frac{1}{2}(2n)^{2}}{\frac{1}{2}n^{2}}=4
\end{align*}$$
So the answer is: about $4$ times longer.
## Orders of Growth
Why consider only the **order of growth** of the operations and roughly discard constants and smaller members ? The running time of an algorithm when the inputs are small is barely recognizable, shit gets real when the input grows arbitrarily, remember the concept of [[Epsilon-Delta Definition of a Limit|limits]] at infinity, if a rational polynomial with tons of factors and degree $n$, if there's a element of degree $n$ on both numerator and denominator, they'll cancel out and all the other terms are irrelevant when input grows to infinity, that's somewhat what happens here. The term with the highest order of growth **dominates** the running time and eventually other terms become so small compared to it that it's not even worth counting.

> "Algorithms that require an exponential number of operations are practical for solving only problems of very small sizes."

Logarithmic growing operations will run **blazingly fast** for any reasonable input size, because basically, when the input doubles in size, the algorithm only adds up one operation, for $n=10^{6}$ a $\log_{2}n$ algorithm will do $\approx 20$ operations.

## Worst-case Best-case and Average-case 

The running time of an algorithm not exclusively depends on the size of the input, but also on some specifics of the input, how it's distributed, organized, etc. For example, on *Sequential Search*, where the algorithm traverses each element of the list until it finds some target $T$, There's some cases:
- Worst-case: The worst possible arrangement of the input is when the target is the last element of the list, therefore bringing the time complexity to $C_{worst}(n)$.
- Best-case: The most optimistic case is when the target is the first element of the list, so the algorithm will only run once: $C_{best}(n)=1$.
- Average-case: The average case is $\frac{n+1}{2}$, the element is somewhere in the middle. Considering some probabilty distributions depending on the input and some other complicated stuff we can derive that.
These things exist to give an idea of the behaviour of an algorithm at it's best, worst, and average cases. It also gives some notion that **not only the worst possible case exists**, and a algorithm efficiency is much clearer analyzing these three situations. Sometimes an overly pessimistic worst case has such a small chance of happening that it almost never happens. If there were only worst case analysis, developers would miss such important insights on analysis.

**Amortized efficiency**

Amortized complexity doesn't apply to a single run of an algorithm but rather to a sequence of operations performed on the same data structure. It turns out that in some situations the total time for an entire sequence of $n$ such operations is always smaller then a worst-case single operation multiplyed by $n$, thus we can "amortize" the high cost of a worst-case occurrence over the entire sequence 