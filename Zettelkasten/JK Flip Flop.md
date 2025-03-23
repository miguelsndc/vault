---
tags: circuits
---
Similar to the SR Flip-Flop, the **JK** Flip-Flop also has two inputs, the outputs are very similar, the JK flip-flop can be **positive edge triggered or negative edge triggered**:

![[Pasted image 20250323161012.png]]

Similar to the **SR** Flip Flop, when both inputs J and K are zero, the state is preserved, when J is 0 and K is 1, the state is reset, and when J is 1 and K is 0, the state is active, however, unlike the **SR**
 Flip Flop that has **indetermined** state when its inputs are both 1, the JK Flip Flop **gets toggled when J and K are both equal to 1**. This type of behaviour finds place in various circuits including **counters**.

### Circuit

![[Pasted image 20250323161638.png]]

### Truth Table

![[Pasted image 20250323161656.png]]

### Characteristic Equation
$$\begin{align*}
Q_{n+1}=J\bar{Q_{n}} + \bar{K}Q_{n}
\end{align*}$$
### Excitation Table

![[Pasted image 20250323161819.png]]

Behaviour is similar to SR Flip Flop, the only great change is the state being toggled when J = K = 1.

### Race Around Condition 

Happens when the clock signal window is very large, and both J and K inputs are active, since the flip flop toggles when inputs are high, it'll keep toggling many times until the clock is low again. that's why the clock window must be very narrow, this is accomplished with the **clock edge** circuit.