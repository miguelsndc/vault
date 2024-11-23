---
tags: ml, ds, dl, stats
aliases: logistic
---
Logistic Regression is a **binary classification** algorithm, even though it's a regression algorithm, it's used to answer classification questions through the use of the [[Sigmoid Function|sigmoid]] function and [[Conditional Probability]] to assign each observation to a class when the probability crosses a certain threshold.

## Formally

Given $X$ as a [[Vector]] of input features, calculate $\hat{y}=P(y=1\mid X)$, where $X\in \R^{nx}$, The parameters of Logistic Regression will be $w \in \R^{nx}$ and $b \in \R$. Then the logistic regression is given by $\sigma(w^{T}+b)$ where $\sigma$ is the [[Sigmoid Function]].
