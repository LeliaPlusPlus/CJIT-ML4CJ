# Logistic Regression

## Motivation
Given a set of features $X$ and binary labels $Y \in (0,1)$, we want a model that can predict the probability that a given sample $x \in X$ has a positive outcome, i.e., $y=1$. For example, we could predict whether or not a student will pass an exam given the amount of hours that they studied. To do so, we can use a logistic regression model. A logistic regression model "uses the logistic function to squeeze the output of a linear equation between 0 and 1" ([Interpretable ML](https://christophm.github.io/interpretable-ml-book/logistic.html)). 

$$logistic(\eta)=\frac{1}{1+exp(-\eta)}$$

## Further Reading
For the logistic regression recitation, please review the [Logistic Regression chapter](https://christophm.github.io/interpretable-ml-book/logistic.html) from the Interpretable ML book and some of the [Gallery Examples](https://scikit-learn.org/1.5/modules/generated/sklearn.linear_model.LogisticRegression.html#gallery-examples) from sklearn.


