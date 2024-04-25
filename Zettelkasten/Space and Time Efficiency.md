---
tags: algorithms
---
Time efficiency or time *complexity* indicates how fast an algorithm runs.
Space efficiency or space *complexity* refers to the amount of memory units required by the algorithm **in addition** to the space needed for it's output and input.

## Units for measuring running time
Counting an algorithm running time on seconds is prone to failure, since execution time in seconds or any unit of time is prone to external factors like: speed of the computer, the quality of the program written, the compiler used to generate machine code, and the difficulty of clocking the actual running time of the algorithm.
Also counting each operation the algorithm does is a *excessivily difficult task* and usually unnecessary. The thing to do is to count how many times the **basic operation** of the algorithm runs. The basic operation is *usually* the most time-consuming task in the algorithm's innermost loop.
