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

> Prediction: *Estimate $\hat{f}$ such that $\hat{Y}$ is as accurate as possible, relationships between variables can be neglected and $\hat{f}$ is treated as a black-box.*
> Inference: *Estimate $f$ such that the relationship between the predictors and the outcomes is as understandable as possible to answer domain questions about the dataset, $\hat{f}$ cannot be treated as black-box.

$a)$

Here we are interested in inference, since no value is required to be predicted. We want to understand better the relationship between the predictors and another variable, in this case, the CEO salary.

We have a $n = 500$ since $500$ firms we're integrated to the investigation, $p=\{ \text{profit}, \text{no\_employees}, \text{industry}, \text{CEO\_salary}\}$, and $|p| = 4$.

This can be treated as a **regression problem**, where we'll model the CEO's salary in function of the other variables, to have a deeper understanding of the underlying relationships.

$b)$ 
This is a classic **prediction** problem with a **classification setting**, we want to predict to which class a product belongs to, *sucess or failure in this case*, based on previous results. $n=20$ and $p$ is a lot of stuff.

$c)$ Prediction with **regression**, we are predicting numerical values.

$3)$

![[ist-plot.excalidraw]]

 - **Test Error**: Has a $U$ shape as flexiblity increases because a extremely restrictive method will naturally have a higher test error since it can't quite grasp the patterns in the data, as we move with flexiblity, we find a sweet spot with the minimal test error possible. As flexibility increases, variance also increases and we overfit the training data.
 - **Training Error**: Training error decreases as we apply more flexible methods because statistical learning methods estimate coefficients to minimize training error, and the most flexible method will likely overfit and have a training error of $0$.
 - **Squared Bias**: Bias decreases as flexibility increases since more flexible methods are capable of capturing the true underlying patterns of the data, but overly flexible methods will have a extremely low bias and will overfit.
 - **Variance:** Restrictive methods have a low variance because, for example, in a linear model, the most noticeable change we'd have in different fits across datasets is a slight change in the slope of the line. More flexible methods tend to have a higher variance due to a high exploitance of the data and potential for overfitting, since they look for more complex patterns in the data, resulting in a high difference in results between datasets.
 - **Bayes error**: The smallest possible test error, given by the [[Bayes Classifier]]. a lower limit to the test error.