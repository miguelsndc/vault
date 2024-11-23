---
tags: dl, ds, ml, stats
aliases: sigmoid
---
The sigmoid function $\sigma(z)$ is a  [[Differentiability and Continuity|continuous]] [[Differentiability and Continuity|differentiable]] [[Functions|function]] that encapsulates a real number and spits out a result between zero and one. 
$$\begin{align*}
\sigma(z)=\frac{1}{1+e^{-z}}
\end{align*}$$
The function is designed such that when $z$ is a very large number, $e^{-z}=1/e^{z}$ will become so small that is nearly neglegibile:
$$\begin{align*}
\lim_{x\rightarrow \infty} \frac{1}{1+e^{-x}}&= \frac{\lim_{x\rightarrow \infty}1}{\lim_{x\rightarrow\infty}1+\lim_{x\rightarrow\infty}e^{-x}}&= \frac{1}{1 + 0}&= 1
\end{align*}$$
And when $z$ is a very large negative number, $e^{-z}$ becomes a huge number, therefore pushing the function down to $0$.

$$\begin{align*}
\lim_{x\rightarrow -\infty} \frac{1}{1+e^{-x}}&= \frac{\lim_{x\rightarrow -\infty}1}{\lim_{x\rightarrow-\infty}1+\lim_{x\rightarrow-\infty}e^{-x}}&= \frac{1}{1 + \infty}&=\frac{1}{\infty}= 0
\end{align*}$$
The graph looks like:
![[Sigmoid Function 2024-11-23 17.43.36.excalidraw]]It intersects the $y$ axis exactly when $\sigma(z)=0.5$.L