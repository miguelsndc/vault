---
tags: binomial-theorem, combinatorics
---
Using [[Pascal's Identity]] and the notion that ${n \choose n}={n \choose 0}$, we can build a special triangle, called **Pascal's Triangle**, where every $k=0,1,2,\cdots,n$ line are the coefficients of the expansion of the [[Binomial Theorem|binomial]] of $k$-th degree. See:
$$\begin{align*}
\begin{matrix}
{0\choose0}\\
{1 \choose 0 }  & {1 \choose 1}\\
{2\choose0} & {2\choose1} & {2 \choose 2}\\
{3 \choose 0}  & {3 \choose 1} & {3\choose2} & {3\choose3}\\
{4\choose0} & {4\choose1} & {4\choose2} & {4\choose3} & {4\choose4}\\
{5\choose0} & {5\choose1} & {5\choose2} & {5\choose3} & {5\choose4} & {5\choose5}\\
{6\choose0} & {6\choose1} & {6\choose2} & {6\choose3} & {6\choose4} & {6\choose5} & {6\choose6}\\
{7\choose0} & {7\choose1} & {7\choose2} & {7\choose3} & {7\choose4} & {7\choose 5} & {7\choose6} & {7\choose7}\\
{8\choose0} & {8\choose1} & {8\choose2} & {8\choose3} & {8\choose4} & {8\choose5} & {8\choose6} & {8\choose7} & {8\choose8}
\end{matrix}=
\begin{matrix}
1\\
1 & 1\\
1 & 2 & 1\\
1 & 3 & 3 & 1\\
1 & 4 & 6 & 4 & 1\\
1 & 5 & 10 & 10 & 5 & 1\\
1 & 6 & 15 & 20 & 15 & 6 & 1\\
1 & 7 & 21 & 35 & 35 & 21 & 7 & 1\\
1 & 8 & 28 & 56 & 70 & 56 & 28 & 8 & 1\\
\end{matrix}
\end{align*}$$
Notice from pascal's identity that, for example on line $k=4$, ${4\choose1}+{4\choose2}={5\choose2}$, Since $4+6=10$.
