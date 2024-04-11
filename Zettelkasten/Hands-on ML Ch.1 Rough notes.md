---
tags: notes
---
"Machine Learning" is the field of study that give computers that ability to learn from data without being explicitly programmed. A program "learns" with experience $E$ with respect to some task $T$, and a performance measure $P$, if it's performance on $T$, as measured by $P$, improves with experience $E$.

The data that the system uses to learn are called the **training set**. Each training example is called a *training instance*, or *sample*.

Machine learning can be used in problems that are either too complex to be solved by hand or do not have any known algorithm, for example, *speech recognition*, one might write a code that knows a couple of words, however, to recognize hundreds of languages spoken by millions of people in noisy environments and in different accents, this quickly becomes an impossible problem. The best approach is to write a machine learning system that learns by itself given **a lot** of voice examples.

Applying machine learning to dig into large amounts of data can help discover patterns that have not yet been discovered, this is called **data mining**.

Machine learning is great for:
- Problems for which solutions require too much hand-tuning or long lists of rules
- Problems that are either too complex or don't have a good solution at all using a traditional approach; *a machine learning algorithm can find a decent solution*.
- Fluctuating environments, machine learning systems adapt to new data
- Getting insights about complex problems and large amounts of data.

# Unsupervised/Supervised Learning

There are four types of learning: ***supervised, unsupervised, semisupervised and reinforcement learning***. 

**Supervised Learning**: The training data you feed the algorithm includes the desired solutions, called **labels**. Two typical supervised learning tasks are **classification:** where the algorithm is given a set of examples and their respective labels/classes, and the algorithm must be able to classify new data into one of those classes.
Another is regression, where the goal is to **predict a target numeric value** given a set of **features** called *predictors*, for example, an algorithm that learns to predict a car price given it's mileage, age, brand, etc.

Examples are:
- k-Nearest neighbors
- Linear Regression
- Logistic Regression
- Support Vector Machines (SVM's)
- Decision Trees and Random Forests
- Neural Networks (Although some variants may be unsupervised)

**Unsupervised learning**: The training data is unlabeled and the algorithm learns without a teacher. Examples of unsupervised learning algorithms:
- Clustering
	- k-Means
	- Hierarchical Cluster Analysis (HCA)
	- Expectation Minimization
- Visualization and *Dimensionality Reduction*:
	- Principal Component Analysis (PCA)
	- Kernel PCA
	- Locally-Linear Embedding (LLE)
	- t-distributed Stochastic Neighbor Embedding (t-SNE)
- Association Rule Learning
	- Apriori
	- Eclat

Clustering algorithms divides data into groups with related features. A Hierarchical clustering algorithm may also subdivide each group into smaller subgroups.

Visualization algorithms are fed a lot of complex, unlabeled and high-dimensional data and output a 2D or 3D representation of the data that can be easily plotted.





















