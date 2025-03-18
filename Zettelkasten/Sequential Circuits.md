---
tags: circuits
---

Circuit where the output not only depends on the present inputs, but also previous states/inputs. A classical example is a counter, where the next state depends on the previous, i.e, previous + 1.

![[sequential.excalidraw]]

A Sequential circuit is basically a combinational circuit that keeps some information stored in memory as binary, then uses both the input and the current state in memory to give the output.

## Asynchronous and Synchronous

**Synchronous sequential circuits** respond to changes in input at discrete time intervals, which are determined by a clock signal. In these circuits, the state of the system (memory) is updated only at specific times, usually at the rising or falling edge of the clock. The combinational logic updates immediately, but the memory elements (like flip-flops) only change state according to the clock.

**Asynchronous sequential circuits**, on the other hand, respond immediately to changes in input without waiting for a clock signal. As soon as the inputs change, the circuit reacts, updating the memory and output after a propagation delay. The state can change at any time, depending on the input changes, and this can lead to more complex timing and potential hazards in asynchronous circuits.