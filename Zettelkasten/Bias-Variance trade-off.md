---
tags: ml, ds
aliases: bias, variance, bias-variance, trade-off
---
There are two fundamental quantities that impact the [[Measuring the Quality of Fit|quality]] of a [[Statistical Learning|statistical learning]] model, called the **bias** and the **variance**.

**Bias** refers to the capability a certain statistical learning method has of capturing the true underlying patterns and shape of a dataset, highly restrictive models like **linear regression**when fit against a wiggly curve will have a **high bias** because it simply can't capture the essence of it.

**Variance** is the difference in accuracy and performance a model shows when tested against different datasets, for example a model that performs greatly in the **training** set but poorly in the **test** set is likely overfitting, and thus has a **high** variance.

The ideal algorithm has both **low bias**, that is, it is sufficiently flexible to capture the essence of the data, but not too flexible to the point it overfits it, and also **low variance**, being capable of showing a reasonably consistent performance across different datasets, the [[Measuring the Quality of Fit|quality]] of the model shouldn't vary crazily when the data is slightly changed.

It is called a trade-off because it is **extremely easy** to, when trying to optimize either the bias or the variance, mess up the counterpart, see, when choosing a more flexible model to reduce bias we might increase variance, when choosing a more restrictive model to lower the variance we might increase the bias and so on, however **there should be** a sweet spot that optimizes both bias and variance, and finding it is the challenge. Notice that we don't know the true form of $f$, the function representing the relationship between the variables of the dataset, so we cannot plot variance nor bias, but it is important to keep this trade-off in mind.
