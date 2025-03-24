---
tags: circuits
---
Since flip-flops can only store 1 bit of information, we use multiple flipflops to store multiple bits of information. Commonly [[D Flip-Flop]]s are used to compose memory elements.

![[Pasted image 20250324092943.png]]

- Theres a tiny issue when handling registers, that is, the time that the data bus is available to fill in the registers, this databus cannot be accessed by any other register, therefore, we use a **load** input as well, that, when true, will make sure the data is written to the flip-flops.