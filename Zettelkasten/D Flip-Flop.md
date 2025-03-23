---
tags: circuits
---
D Flip-Flop is a **edge triggered** sequential circuit, also **synchronous**, since it responds only to inputs only on the **transition** of the clock circuit.

#### Circuit and Truth Table
The flip-flop can be implemented with the help of the [[SR Latch]], a **latch** can be made synchronous by connecting the enable input to the clock signal, and that is the sr flip flop, but for the **D** Flip-Flop, since it receives a single input D that dictates the transitions, the following can be done:

![[flipflopd.excalidraw]]


As in [[SR Latch]], the output $Q$ follows the input $S$ and $Q'$ follows $R$, and when both are zero the state is preserved, but by connecting the input **D** to $S$ and it's negation to $R$, now the gate responds solely to the $D$ input, and preserves state when the clock is off.

#### Truth Table:

![[Pasted image 20250323152710.png]]


