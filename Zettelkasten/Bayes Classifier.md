---
tags: ml, ds, stats
aliases: bayes
---
The Bayes classifier leverages [[Bayes' Theorem]] and [[Conditional Probability]] to solve the classification problem, it is the classification method with smallest test error rate. It works by, given a [[Vector|vector]] of predictors $x_{0}$, it uses conditional probability to assign those observations to a class $j$, using:
$$\begin{align*}
\P(Y=j\mid X=x_{0})
\end{align*}$$
It is a two-class problem, and if $\P(Y=j \mid X=x_{0}) > 0.5$ it's assigned to class $1$, and assigned to class $2$ otherwise.The error rate is given by $1-\max_{j}(\P(Y=j\mid X=x_{0}))$ at $X= x_{0}$.*(Since it works by separating points given a certain probability, the error rate will be the probability of missing the assignments we're most certain of)* 