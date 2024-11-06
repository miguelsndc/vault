---
tags: ml, ds, stats
aliases: k-nearest
---
In reality we can't use the optimal [[Bayes Classifier]], so it ends up being a gold standard against which we compare other methods, since we cannot find the true conditional probability, several methods that calculate a *estimated* probability were invented, such as the one being discussed here:

**K-Nearest Neighbours** method classifies observations based on proximity, Given a integer $K$ and a test observation $x_{0}$, first it identifies the $K$ points in the dataset closest to $x_{0}$, let's label them $\aleph_{0}$. Then it approximates the conditional probability of $\P(Y=j\mid X=x_{0})$ as the sum of all [[Indicator Function|indicator]] variables of $Y=j$ of $\aleph_{0}$ averaged by $K$:
$$\begin{align*}
\P(Y=j\mid X=x_{0})=\frac{1}{K}\sum\limits_{i\in \aleph_{0}}I(y_{i}=j)
\end{align*}$$
Despite it's simplicity, this algorithm has shown error rates incredibly close to the bayes classifier, but there are some gotchas
___
## Choice of $K$

The parameter $K$ introduced before is fundamental to the algorithm, lower choices of $K$ imply a **highly** flexible run with low bias, but a **high** variance, being extremely prone to overfitting, and higher choices of $K$ have very high bias, not being capable to detect the true patterns behind the data, with a **low** variance in return, this resembles once more the [[Bias-Variance trade-off]], as a optimal choice of $K$ has to be made, so that the test error rate is minimized as much as possible.
