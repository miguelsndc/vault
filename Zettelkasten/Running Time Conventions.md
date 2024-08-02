---
tags: algorithms
---
The **running time** of an algorithm on a particular input is the number of instructions and data accesses used. 
How we account for the time taken of each of these instructions should be independent of the computer, but, let's adopt this view:
- Each line of code takes a constant time $c_{k}$ to run.
- If a line is executed $m$ times, then the time taken by that part is $c_{k}m$, Although this might not be exactly true, specially refering to memory, a statement referencing $m$ words of memory $n$ times does not necessarily takes $mn$ time.
- A statement that calls a subroutine takes constant time, however, the subroutine itself may take more than constant time, that's why we separate the process of **calling** the subroutine, passing parameters to it, etc, from actually **running** the subroutine.
