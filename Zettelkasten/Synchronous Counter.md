---
tags: circuits
---
Does what the name says, counts. if we want to have a **binary counter** that can count up to $2^{n}-1$ we need **n** flip-flops connected in parallel to the same clock sifnal
#### Steps to build a counter:
1. Find the required number of **flip-flops**.
2. Draw the **state diagram**
3. Select the flip-flop type and draw the excitation table
4. Find minimal expression for the excitation of each flip-flop
5. Draw the circuit

For the JK flipflop the equations for $n$ bit counters are:
$$\begin{align*}
\begin{cases}
J_0=K_0=1\\
J_1=K_1=Q_{}0\\
Jn=Kn=Q_{n-1}\cdots Q_{0}
\end{cases}
\end{align*}$$
And the propagation delay of this Synchronous counter is $T_{pd}(FF) + (n-2)T_{pd}(\textrm{AND})$, where $T_{pd}$ stands for time of propagation delay.