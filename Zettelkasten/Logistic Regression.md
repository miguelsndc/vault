---
tags: ml, ds, dl, stats
aliases: logistic
---
Logistic Regression is a **binary classification** algorithm, even though it's a regression algorithm, it's used to answer classification questions through the use of the [[Sigmoid Function|sigmoid]] function and [[Conditional Probability]] to assign each observation to a class when the probability crosses a certain threshold.

## Formally

Given $X$ as a [[Vector]] of input features, calculate $\hat{y}=P(y=1\mid X)$, where $X\in \R^{nx}$, The parameters of Logistic Regression will be $w \in \R^{nx}$ and $b \in \R$ where $nx$ is the [[Theorems and Proofs for Basis and Dimension|dimension]] of the input feature vector. Then the logistic regression is given by $\sigma(w^{T}+b)$ where $\sigma$ is the [[Sigmoid Function]].

## Cost Function

To train and assess the quality of the Logistic Regression Model, we need to define a **cost function**, a [[Functions|function]] that will determine how well the model performs.

Given a training set $\{(x^{(1)},y^{(1)}), (x^{(2)},y^{(2)}), \cdots, (x^{(m)},y^{(m)})\}$, we want $\hat{y}^{(i)}\approx y^{(i)}$, i.e our predictions to be as close as possible to the actual value, at least in the training set.

Here we can define a **Loss (error)** as squared error: $\mathcal{L}(\hat{y}, y)=\frac{1}{2}(\hat{y} - y)^{2}$, but this is not generally used in logistic regression because it makes the optimization problem **non-convex**, so the **gradient descent** might get stuck at a bad **local minima**, because the [[Sigmoid Function]] is non-linear. Squared error works great for linear regression, but not here, instead we use:
$$\begin{align*}
\mathcal{L}(\hat{y}, y)=-(y\log\hat{y} + (1-y)\log(1-\hat{y}))
\end{align*}$$
