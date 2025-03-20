---
tags: circuits
---
Latches and flip-flops are memory elements capable of storing 1-bit of information at a time. The difference between latches and flip-flops is that latches are [[Sequential Circuits|asynchronous]], that is, respond **immediately** to changes in input, while flip-flops are [[Sequential Circuits|synchronous]] and only change on discrete time intervals.

**Transparent Latches** are the asynchronous ones. Transparent latches can also be made synchronous by connecting a **enable** input gate at the latch and connecting it to the clock signal. this way, the latch will only beoome transparent when the clock signal is high, therefore making it a **level triggered** circuit.

Look at the diagram:
![[gated-latch.excalidraw]]
