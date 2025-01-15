# Logistic Regression

## Motivation
Given a set of features $X$ and binary labels $Y \in (0,1)$, we want a model that can predict the probability that a given sample $x \in X$ has a positive outcome, i.e., $y=1$. For example, we could predict whether or not a student will pass an exam given the amount of hours that they studied. To do so, we can use a logistic regression model. A logistic regression model "uses the logistic function to squeeze the output of a linear equation between 0 and 1" ([Interpretable ML](https://christophm.github.io/interpretable-ml-book/logistic.html)). The logistic (or sigmoid) function is defined as:

$$logistic(\eta)=\frac{1}{1+exp(-\eta)}$$

Thus, our model learns the following equation:
$$P(y=1)=\frac{1}{1+exp(-(\beta_0 + \beta_1 x_1 + ... + \beta_p x_p))}$$

We can use the threshold $0.5$ to determine to which class a point belongs given our model's predicted probability. 

## Interpretation


The odds ratio should not interpreted outside of its intended meaning.

!["Example graph of a logistic regression curve fitted to data. The curve shows the estimated probability of passing an exam (binary dependent variable) versus hours studying (scalar independent variable)", caption courtesy of Wikipedia](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/logisticregression/imgs/Exam_pass_logistic_curve.png)

## Further Reading
For the logistic regression recitation, please review the [Logistic Regression chapter](https://christophm.github.io/interpretable-ml-book/logistic.html) from the Interpretable ML book and some of the [Gallery Examples](https://scikit-learn.org/1.5/modules/generated/sklearn.linear_model.LogisticRegression.html#gallery-examples) from sklearn.

## Citations
- [Logistic Regression - Interpretable ML Book](https://christophm.github.io/interpretable-ml-book/logistic.html)
- [Logistic Regression - Wikipedia](https://en.wikipedia.org/wiki/Logistic_regression)
