---
tags: circuits
---
We can implement 1-bit memory element using **logic gates** by connecting the gates to themselves, so they preserve information, we can change which values get stored by toggling an input value.

### SR Latch

![[sr-latch.excalidraw]]

| S   | R   | Q       | Q'      |     |
| --- | --- | ------- | ------- | --- |
| 0   | 0   | Remains | Remains |     |
| 0   | 1   | 0       | 1       |     |
| 1   | 0   | 1       | 0       |     |
| 1   | 1   | Invalid | Invalid |     |
The outputs of the **SR** Latch are always **complementary**, if $A = Q$ then $B = \bar{Q}$.

## Gated SR Latch
Apart from the S and R inputs, the Gated SR Latch also receive an **enable input**, that decides when the latch will respond to change.


![[Pasted image 20250323140345.png]]

The enable is connected with and **AND** gate to the S and R inputs, the yellow square highlights the actual SR Latch.

![[Pasted image 20250323140436.png]]



