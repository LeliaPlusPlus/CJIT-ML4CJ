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

![A decision tree for playing outside based on the weather](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/ensembles/imgs/GEP_decision_tree_with_numeric_and_nominal_attributes.png)

## Ensemble Methods
Unfortunately, one decision tree tends to overfit the data. In order to prevent overfitting, we can create ensembles of decision trees. Ensembles mean we use more than one model. We can use multiple of the same model for a homogeneous ensemble (e.g., random forests) or different models for a hetergeneous ensemble (e.g., superlearners).  
Ensemble methods include:
<ul> 
<li> Bagging: </li>
<li> Boosting: </li>
<li> Stacking: </li>
</ul>

## Random Forest


## XGBoost



## Citations
[Decision tree learning - Wikipedia](https://en.wikipedia.org/wiki/Decision_tree_learning)  
[Chapter 5.4: Decision Tree](https://christophm.github.io/interpretable-ml-book/tree.html) in the Interpretable Machine Learning Book by Christopher Molnar  
Friedman, Jerome, Trevor Hastie, and Robert Tibshirani. “The elements of statistical learning”. hastie.su.domains/ElemStatLearn (2009).  
Images courtesy of Wikimedia Commons.

