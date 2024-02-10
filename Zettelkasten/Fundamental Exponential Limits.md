---
tags: limits
---
The fundamental [[Epsilon-Delta Definition of a Limit|limits]] of exponential are:
- $\lim_{x\rightarrow0} \frac{\rm{e}^{x}-1}{x}=1$ 
## Proof:
$$\begin{align*}
&\lim_{h\rightarrow0}\frac{e^{h}-1}{h}\\
&\text{Let } \rm{e}^{h}-1= x\\
&\implies e^h=x+1\\
&\implies \ln{e^{h}} =\ln{x+1}\\
&\implies h=\ln{x+1}\\
&(h \rightarrow 0 \implies x \rightarrow)\\
\lim_{h\rightarrow0} \frac{h}{\rm{e}^{h-1}}&= \lim_{x\rightarrow0} \left[\frac{1}{x} \cdot \ln{x+1}\right]=\lim_{x\rightarrow0}\ln(1+x)^{\frac{1}{x}}\\
&= \ln(\lim_{x\rightarrow0} (1+x)^\frac{1}{x})\\
&= \ln{\rm{e}}=1
\end{align*}$$
