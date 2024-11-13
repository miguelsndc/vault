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

$4)$ 
Classification is the **categorical** setting of regression, since classification, by definition, tries to predict to which "class" or category a certain predictor belongs to.

1. Tell which type of **cancer** a patient is likely to have, given a set of exams and measurement, is a classification problem, since we're trying to fit the observations into groups. It's a prediction problem.
2. Tell, given a text, what is the **sentiment** of that text given the words and context used in it, anger, sadness, etc. It's a prediction problem.
3. Predict the type of papaya, given a picture. Prediction.


$b)$ 

1. Predict the profit of a company in upcoming years given past years and market data. Prediction.
2. Predict the probability of kidney failure of a kitty given data about the cat, like height, weight, average ml of water drank per day etc. Prediction.
3. Predict the expected height of a tree given the species, geographic location, type of tree, etc.


$c)$
1. Market Segmentation.
2. Group users of a platform by geographic location / age, etc.
3. Given fire data about a certain geographic location, group by intensity / frequency etc, to understand which areas suffer the most .

$5)$ A more flexible approach in both regression and classification has the advantage of being more sensitive to patterns in the data, therefore being capable of perceiving things more restrictive models can't. A more flexible approach might be preferred when we have a highly non-linear dataset, that exhibits a very complex relationship between it's predictors. A restrictive model cannot capture that.
A less flexible method is preferred when the relationship between the variables is not complex enough to require a flexible model or when the number of samples is not large enough to feed a flexible model, so a less flexible method will function better with that limited sample, since it doesn't go too deep and usually requires an assumption.

$6)$ A **parametric** statistical learning approach requires an assumption about the shape of the underlying function $f$. Given this assumption, a parametric approach reduces the problem of finding a whole $n$-dimensional function $f$, to estimating a set of coefficients $\beta_{0}, \cdots, \beta_{n}$ that dictate the behaviour of $f$ inside the restrictions imposed by the assumptions. 
A **non**-parametric statistical learning approach makes zero assumptions about the shape of $f$ and simply tries to find the best possible estimate to fit the data, this is a more flexible method that requires an injuriating amount of samples to be consistent, and has a high potential for overfitting. The only parameters a engineer can tweak are possibly the level of smoothness of the function, so it doesn't get too rough of too wiggly.