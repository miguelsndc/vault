---
tags: trigonometry
---
Let us find (and prove) the sine of sum $\sin(A+B)$ using [[Euler's Formula]]:
$$
\begin{align*}
\cos(x)+i\sin(x) &= e^{ix}\\
\cos(A+B) + i\sin(A+B) &= e^{i(A+B)}\\
\cos(A+B)+i\sin(A+B) &= e^{iA+iB}\\
\cos(A+B) + i\sin(A+B)&= e^{iA}e^{iB}\\
\cos(A+B) + i\sin(A+B)&= (\cos(A) + i\sin(A))(\cos(B)+i\sin(B))\\
\cos(A+B) + i\sin(A+B)&= \cos(A)\cos(B)+\cos(A)i\sin(B)+i\sin(A)\cos(B)+i^{2}\sin(A)\sin(B)\\
\cos(A+B) + i\sin(A+B)&= \cos(A)\cos(B)+\cos(A)i\sin(B)+i\sin(A)\cos(B)-\sin(A)\sin(B)\\
\end{align*}
$$
Now we separate the [[Complex Numbers|imaginary]] part from the [[Real Numbers|real]] part.
$$\begin{align*}
=\cos(A)\cos(B)+\cos(A)i\sin(B)+i\sin(A)\cos(B)-\sin(A)\sin(B)\\
= \cos(A)\cos(B)-\sin(A)\sin(B)+i(\cos(A)\sin(B)+\cos(B)\sin(A))
\end{align*}$$
So we now that the cosine is the real part and the sine is the imaginary part, so it follows that:
$$\begin{align*}
\sin(A+B)&= \sin(A)\cos(B)+\cos(A)\sin(B)\\
\cos(A+B)&= \cos(A)\cos(B)-\sin(A)\sin(B)
\end{align*}$$
>[!tip] Sine and Cosine of Sum:
>From Euler's formula we derive:
>$$\begin{align*}
\sin(A+B)&= \sin(A)\cos(B)+\cos(A)\sin(B)\\
\cos(A+B)&= \cos(A)\cos(B)-\sin(A)\sin(B)
\end{align*}$$

>


