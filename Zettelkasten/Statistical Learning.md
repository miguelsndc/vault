---
tags: ds, ml
---
**Statistical Learning** refers to a set of tools and techniques used to estimate the relationship between a set of **variables** or **features** of a collection of measurements *(the dataset)*, we can state a more tied up definition:

*Given a set of $p$ called predictors $X=(X_{1}, X_{2}, \cdots, X_{p})$  and $Y$, called the response variable, statistical learning refers to the process of estimating $f$ such that $Y=f(X) + \epsilon$.

There are two reasons we want to estimate $f$: *Prediction* and *Inference*.

**Prediction**
Suppose a set of inputs whose output is not easily obtained, in this case, since $\epsilon$ averages to zero, we can treat the output $\hat{Y}$ representing $Y$, being purely a function $\hat{f}$ (represeting $f$) of $X$. $\hat{Y} = \hat{f}(X)$. In this setting, $\hat{f}$ can be treat as a **black-box**, meaning that one's not concerned about the exact form of $\hat{f}$, provided that it yields accurate predictions for $Y$.

The accuracy of $\hat{Y}$ as a model for $Y$ depends on two quantities, the *irreducible error* and *reducible error*. The latter can be minimized by choosing a more appropriate statistical learning tool, collecting more data, etc. The first **cannot** be minimized, recall that $Y$ is also a function of $\epsilon$, and $\epsilon$ represents all the error that is naturally introduced into $Y$, such as measurement errors, uncollectible data, missing variables, etc, all those factors reinforce that $\hat{f}$ won't ever be a perfect estimate of $f$.

**Inference**
Sometimes, one is not interested exactly in predicting the outcome $Y$ from a set of inputs $X_{1}\cdots, X_{p}$, but rather understanding the relationship between each variable and the output. We still want (and need) to estimate $f$, however, this time we cannot treat $f$ as a black-box, now we must find an accurate (as much as possible) representation of $f$.

Question like: *"How much does variable $X_{n}$ affect the outcome ?"*, *"Which variables have the most impact on the outcome ? Which can be discarded ?"*, Questions that arise from a seek of understading the relationship between each predictor and the outcomes fall into the **inferece** category.
___
We can summarize the approaches as follows:

Prediction: *Estimate $\hat{f}$ such that $\hat{Y}$ is as accurate as possible, relationships between variables can be neglected and $\hat{f}$ is treated as a black-box.*
Inference: *Estimate $f$ such that the relationship between the predictors and the outcomes is as understandable as possible to answer domain questions about the dataset, $\hat{f}$ cannot be treated as black-box.*

Problems might fall on one or both categories, they're not mutually exclusive.

## How to estimate $f$ ?

To estimate $f$ we'll assume we have a set of $n$ observations, and each observation is a pair of inputs/output: Let $i$ represent the $i$th observation, then $(x_{i},y_{i})$, where $x_{i}=(x_{i1},x_{i2},\cdots,x_{ip})^{T}$ is the input with $p$ predictors and $y_{i}$ the associated response. the [[[Sets|set]] $\{(x_{1},y_{1}), (x_{2},y_{2}), \cdots, (x_{n}, y_{n})\}$ is called the **training** data, we'll use it to *teach* our method to estimate $f$. Our goal is to apply a method to the training data in order to estimate an unknown function $f$. In other words, we want to find a function $\hat{f}$ where $Y \approx \hat{f}(X)$ for any $(X,Y)$. Broadly speaking, any statistical learning method can be characterized as either *parametric* or *non-parametric*.