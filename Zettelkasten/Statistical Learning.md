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
Sometimes, one is not interested exactly in predicting the outcome $Y$ from a set of inputs $X_{1}\cdots, X_{p}$, but rather understanding the relationship between each variable and the output. We are still interested in estimating $f$, however, this time we cannot treat $f$ as a black-box, but now we must find an accurate representation of $f$.

Question like: *"How much does variable $X_{n}$ affect the outcome ?"*, *"Which variables have the most impact on the outcome ? Which can be discarded ?"*, Questions that arise from a seek of understading the relationship between predictors and results fall into the **inferece** category.

