---
tags: ml, ds
aliases: quality
---
In order to evaluate the performance of a [[Statistical Learning]] method, we need some procedure to measure the accuracy of the method, a very common one is the $\text{MSE}$, *Mean Squared Error* method:
$$\begin{align*}
\text{MSE} &= \frac{1}{N}\sum\limits_{i=1}^{n} (y_{i}-\hat{f}(x_{i}))^{2}
\end{align*}$$
Think of it like:
1. To measure the quality of a estimate $\hat{f}$ for $x_{i}$, we can find the difference between the actual value $y_{i}$ and $\hat{f}(x_{i})$.
2. Staticians don't like negative numbers, so we square it.
3. To assess this across for all observations, we can sum the values for all pairs of actual value / model prediction.
4. This number would be kind of big and weird to look at *(imagine telling someone the accuracy of your model is $762.85$ lol)*, by taking the average we reduce that number to a reasonable interval and find out the average error of the model, this number being much better to deal with, notice that this implies a sensitivity to outliers.
5. So the smaller the averaged sum of squared differences between model predictions and responses the better the model is, quite simple.

On creating models we are more interested on those whose performance is best on **unseen, test data**, than on training data, the algorithms are developed such that the *MSE* is minimized during training, and all methods will have a good performance when put against this scenario, however not all of them will have a performance as good as the one put up in the training stage.

So how do we select the best statistical learning method for the problem ? In some settings, we may have some **test** data, unused during training, that we run the model against and measure the performance, and the model with the smallest *MSE* is chosen. This is not always the case, so choosing a model that performs the best on training data should be the natural answer, but in reality this isn't the case, most of the time the models performing best on training data do not perform as well on real, unseen data, this phenomenom is called **overfitting**, when the model fails to capture the true essence of the relationship between variables and outcomes, and instead molds itself to best perform on that specific dataset.

