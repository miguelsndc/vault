---
tags: circuits
---
Latches and flip-flops are memory elements capable of storing 1-bit of information at a time. The difference between latches and flip-flops is that latches are [[Sequential Circuits|asynchronous]], that is, respond **immediately** to changes in input, while flip-flops are [[Sequential Circuits|synchronous]] and only change on discrete time intervals.

**Transparent Latches** are the asynchronous ones. Transparent latches can also be made synchronous by connecting a **enable** input gate at the latch and connecting it to the clock signal. this way, the latch will only beoome transparent when the clock signal is high, therefore making it a **level triggered** circuit.

Look at the diagram:
![[gated-latch.excalidraw]]
**Flip-flops** on the other hand are **edge triggered** circuits, they respond to the input when the clock is **rising** or **falling**, depending on which type of flip-flop it is:
- **Negative edge triggered** flip-flops are high when the input is high and the clock is on falling stage, and will remain in that state until the next falling stage, if the input is low then the flip-flop will be low and vice-versa;
- **Positive edge triggered** flip-flops are respond when to the input when the clock is on rising stage.

> Flip-flops can be implement by connecting the **enable** gate of the **Gated Latch** to the **clock transition** circuit.
