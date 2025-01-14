---
tags: ml, ds, stats
aliases: bayes
---
The Bayes classifier leverages [[Bayes' Theorem]] and [[Conditional Probability]] to solve the classification problem, it is the classification method that gives the smallest possible test error rate. It works by, given a [[Vector|vector]] of predictors $x_{0}$, conditional probability is used to assign those observations to a class $j$, using:
$$\begin{align*}
\P(Y=j\mid X=x_{0})
\end{align*}$$
In a two-class problem, if $\P(Y=j \mid X=x_{0}) > 0.5$, $x_{0}$ is assigned to class $1$, otherwise class $2$.The error rate is given by $1-\max_{j}(\P(Y=j\mid X=x_{0}))$ at $X= x_{0}$, the bayes' error rate is the probability of $x_{0}$ **not** belonging to the most likely class *(so it missed)*:
$$\begin{align*}
1-E(\max_{j}\P(Y=j \mid X))
\end{align*}$$

When the probabilities of certain points turn out to be equal, this [[Vector Space|space]] is called the **Bayes decision boundary**, it's where we're equally uncertain between two classes. Usually it is not possible to use the bayes classifier because we need to know the **distribution** of $Y$ given $X$, so the bayes classifier is out of choice.