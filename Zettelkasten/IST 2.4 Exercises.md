---
tags: ml, ds, stats
---

$1)$ State whether we would expect the flexible method to perform better than the inflexible method in the given context, justify.
- Sample size $n$ is extremely large, the number $p$ of predictors is small.

We can expect the flexible method to perform better, a usually a flexible method needs a astonishingly large amount of data to be correctly trained, here we have it, and since the number of predictors is small, the relationship between the variables is consequently simpler, therefore we can expect the method to identify the correct relationship with relative ease.

- The number of predictors $p$ is large, and the number of samples $n$ is small

A large number of predictors implies on a complex relationship between the variables, and since we don't have enough data to teach a flexible model too well, it'll very likely overfit and perform terribly on test data. We can make an assumption about this data and apply a more restrictive method, that'll likely perform better with the correct assumption.

- The relationship between predictors and response is highly non-linear

We definetly can't fit a line thorugh this data, so a more flexible method is definetely required, probably a smooth spline will do the job well. Therefore flexible will perform better (with appropriate smoothness level)

- The [[Bias-Variance trade-off|variance]] of the error term is extremely large.

We need a method with the correct [[Bias-Variance trade-off]], i firmly believe that a linear model cannot capture the true essence of this data, so a more flexible method has to be used, depends on the data actually, but definetely a more flexible method, not too flexible though, or it will overfit.

2) Explain whether each scenario is a classifcation or regression problem, and indicate whether we are most interested in inference or prediction. Finally, provide $n$ and $p$.

- *"We collect a set of data on the top $500$ firms in the US. For each firm we record profit, number of employees, industry and the CEO salary. We are interested in understanding which factors affect CEO salary"*

> Prediction: *Estimate $\hat{f}$ such that $\hat{Y}$ is as accurate as possible, relationships between variables can be neglected and $\hat{f}$ is treated as a black-box.*
> Inference: *Estimate $f$ such that the relationship between the predictors and the outcomes is as understandable as possible to answer domain questions about the dataset, $\hat{f}$ cannot be treated as black-box.

Here we are interested in inference, since no value is required to be predicted. We want to understand better the relationship between the predictors and another variable, in this case, the CEO salary.

We have a $n = 500$ since $500$ firms we're integrated to the investigation, $p=\{ \text{profit}, \text{no\_employees}, \text{industry}, \text{CEO\_salary}\}$, and $|p| = 4$.

This can be treated as a **classification problem**. We can separate the different salary ranges and throw the CEO's there, and analyze the common characteristics of firms with CEO's in the same salary range, via clustering and other techniques.