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
___
Types of training.
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

Dimensionality reduction takes high-dimensional data and tries to simplify the data as much as possible without losing too much information. One example is to merge correlated features, $e.g$, a car's mileage may be very well correlated with it's age, a dimensionality reduction algorithm will merge these features into one that represents the whole thing.

Anomaly detection, as said, detects anomalies/outliers in data, for example, to prevent frauds or automatically remove outliers from data. The system's trained with normal instances and when it sees a new instance it can tell whether it **looks like a normal one** or is an anomaly.

Association rule learning digs into large amounts of data and detects relations between attributes.

**Semisupervised learning**: Some algorithms can deal with partially labeled training data. Most semisupervised algorithms are combinations of supervised and unsupervised algorithms. deep belief networks DBN's for example.


**Reinforcement learning**: The learning system, called an agent can observe the environment, select and perform actions, and get *rewards* in return (or *penalties* in form of negative rewards). It must then learn by itself what's the best strategy to get the most reward of time.

# Online/Batch Learning

On batch learning the system must be trained from scratch with all the available data, then it is launched into production and doesn't learn anymore, just applies what it has learned, this is called **batch learning**.

- Requires a lot of CPU, Network I/O, disk I/O and memory resources.

Online or incremental learning: you train the system incrementally by feeding it data instances sequentially, either individually or by small groups called *mini-batches*.
- Reduces computational costs by a fair amount
- Good for systems that require continuous flow
- Can be used to train huge datasets that may not fit in a computer's memory
How fast it should adapt to new data is defined by a parameter called *learning rate*, if the learning rate is high, it adapts quickly to new data, but may forget old data. If set low, the system will learn slower and have more inertia, that is, it'll be less sensitive to outliers. It's possible to

# Instance vs. Model based learning

How it generalizes

On instance based learning the algorithm learns everything by heart, for example it could flag as spam only emails that are identical to the already flagged ones, or could use some **similarity measure** such as the count of words, or some common words that appear in spams. Basically it learns the examples by heart, then generalizes to new cases using a similarity measure.

Another way to generalize is to build a model of these examples, then use to model to make predictions. You first analyze and understand the data to detect patterns and trends, then you choose an algorithm that better exploits these patterns and build a model out of it, then use that model to predict new values.

# What can go wrong ?

- Insufficient amounts of data.
- Nonrepresentative data, that is, the data you gathered may not represent the reality due to 