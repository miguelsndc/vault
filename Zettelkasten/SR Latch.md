---
tags: circuits
---
We can implement 1-bit memory element using **logic gates** by connecting the gates to themselves, so they preserve information, we can change which values get stored by toggling an input value.

### SR Latch

![[sr-latch.excalidraw]]

| S   | R   | B                         |
| --- | --- | ------------------------- |
| 0   | 0   | Remains in Previous State |
| 1   | 0   | 1                         |
| 0   | 1   | 1                         |
| 1   | 1   | X                         |
The outputs of the **SR** Latch are always **complementary**, if $A = Q$ then $B = \bar{Q}$.
