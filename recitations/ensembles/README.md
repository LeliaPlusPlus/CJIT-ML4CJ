# Ensembles in Machine Learning

## Problem Setup
Let's consider the supervised learning setting.  
  
Given a set of features $x \in X$ and labels $y \in Y$, we want to learn $f(x)$ under the objective function $min \left|f(x)-y \right|$.  

In machine learning, we have a train and test set to understand if our model generalizes by not over or underfitting the data.  

Supervised learning can be generally divided into two categories: classification in which the target is discrete (e.g., logistic regression), and regression in which the target is continuous (e.g., linear regression).

## Decision Tree
In supervised machine learning, a decision tree is a representation of data with a [tree](https://en.wikipedia.org/wiki/Tree_(abstract_data_type)#Terminology) that explicitly outlines decisions. Decision trees allow us to learn non-linear representations of data.  

Let's consider the classification setting. In a classification tree, split (or internal) nodes represent conjunctions of features, and leaf (or terminal) nodes represent class labels. To create different branches (or splits), tree-based models iteratively split the data "according to certain cutoff values in the features" ([Molnar](https://christophm.github.io/interpretable-ml-book/tree.html)). Splitting results in subsets of the data in which each sample belongs to one subset.  

The below image represents a decision tree for playing outside based on the weather. 

![A decision tree for playing outside based on the weather](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/ensembles/imgs/Decision_tree_for_playing_outside.png)

## Ensemble Methods
Unfortunately, one decision tree tends to overfit the data. In order to prevent overfitting, we can create ensembles of decision trees. Ensembles mean we use more than one model. We can use multiple of the same model for a homogeneous ensemble (e.g., random forests) or different models for a heterogeneous ensemble (e.g., superlearners). We cover the bagging and boosting methods based on two popular tree methods. 

### Random Forest
With bootstrap aggregating (bagging), we simultaneously build multiple decision trees by repeatedly resampling training data with replacement, and voting the trees for a consensus prediction. Random forest is an ensemble of bagged decision trees. "For classification tasks, the output of the random forest is the class selected by most trees. For regression tasks, the output is the average of the predictions of the trees." [Wikipedia](https://en.wikipedia.org/wiki/Random_forest)
![A figure demonstrating how bagging works.](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/ensembles/imgs/Ensemble-Bagging.png)

### XGBoost
With boosting, we train multiple models sequentially. In each new sequence, we train a model to emphasize the training samples that were previously mis-classified. To start, we equally weight all training samples and input them into a model. For those mis-classified samples, we upweight (i.e., increase their weight) them to encourage the model to focus on these samples and correctly classify them. The final model is a weighted sum of the learners.  

Boosting may be computationally intensive. We can use gradient descent to compute the gradient of the loss of our ensemble. Even further, XGBoost (eXtreme Gradient Boosting) further speeds up computation through various mechanisms [Wikipedia](https://en.wikipedia.org/wiki/XGBoost). 

![A figure demonstrating how boosting works.](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/ensembles/imgs/Ensemble-Boosting.png)

## Citations
[Decision tree learning - Wikipedia](https://en.wikipedia.org/wiki/Decision_tree_learning)  
[Chapter 5.4: Decision Tree](https://christophm.github.io/interpretable-ml-book/tree.html) in the Interpretable Machine Learning Book by Christopher Molnar  
Friedman, Jerome, Trevor Hastie, and Robert Tibshirani. “The elements of statistical learning”. hastie.su.domains/ElemStatLearn (2009).  
Images courtesy of Wikimedia Commons.

## Further Reading
[What is Boosting? - AWS](https://aws.amazon.com/what-is/boosting/)
[Gradient Boosted Decision Trees](https://developers.google.com/machine-learning/decision-forests/intro-to-gbdt)
