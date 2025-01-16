# Logistic Regression

## Motivation
Given a set of features $X$ and binary labels $Y \in (0,1)$, we want a model that can predict the probability that a given sample $x \in X$ has a positive outcome, i.e., $y=1$. For example, we could predict whether or not a student will pass an exam given the amount of hours that they studied. To do so, we can use a logistic regression model. A logistic regression model "uses the logistic function to squeeze the output of a linear equation between 0 and 1" ([Interpretable ML](https://christophm.github.io/interpretable-ml-book/logistic.html)). The logistic (or sigmoid) function is defined as:

$$logistic(\eta)=\frac{1}{1+exp(-\eta)}$$

Thus, our model learns the following equation:  

$P(y=1)=\frac{1}{1+exp(-(\beta_0 + \beta_1 x_1 + ... + \beta_p x_p))}$

We can use the threshold $0.5$ to determine to which class a point belongs given our model's predicted probability. 

!["Example graph of a logistic regression curve fitted to data. The curve shows the estimated probability of passing an exam (binary dependent variable) versus hours studying (scalar independent variable)", caption courtesy of Wikipedia](https://github.com/LeliaPlusPlus/CJIT-ML4CJ/blob/main/recitations/logisticregression/imgs/Exam_pass_logistic_curve.png)

## Interpretation
According to the [Interpretable ML](https://christophm.github.io/interpretable-ml-book/logistic.html) book, "The interpretation of the weights in logistic regression differs from the interpretation of the weights in linear regression, since the outcome in logistic regression is a probability between 0 and 1. The weights do not influence the probability linearly any longer. The weighted sum is transformed by the logistic function to a probability. Therefore we need to reformulate the equation for the interpretation so that only the linear term is on the right side of the formula."  

$ln(\frac{P(Y=1)}{1-P(Y=1)})=log(\frac{P(Y=1)}{P(Y=0)})=\beta_0 + \beta_1 x_1 + ... + \beta_p x_p$

This above equation shows the log odds. Odds refers to the likelihood that an event occurs, or the probability that an event occurs divided by the probability that the event does not occur. While the above equation gives us the log odds, we want to know how the prediction changes when one of the features $x_j$ is changed by 1 unit ([Interpretable ML](https://christophm.github.io/interpretable-ml-book/logistic.html)). Thus, we can apply the inverse of the log to both sides of the equation with the exponential function:  

$\frac{P(Y=1)}{1-P(Y=1)}=odds=exp(\beta_0 + \beta_1 x_1 + ... + \beta_p x_p)$

When we output a model, we can actually take the exponential of the coefficients to get the odds ratio. An odds ratio of one means the outcomes are equally likely. However, the coefficients are still useful to interpret on their own. The importance of coefficients can be interpreted based on their direction and magnitude. For example, a feature with a coefficient of 5 has a higher importance for the outcome than a feature with a coefficient of 2.

## Machine Learning Approach
Logistic regression is a widely used tool in both statistics and machine learning, including estimation, prediction, risk quantification, and causal inference. However, the two approaches can differ.  

In machine learning, we often want a model that can generalize on some held out test set. We assess this generalization through performance metrics (e.g., accuracy, error, area under the reciever operating curve, precision, recall, etc.) and loss curves. We believe a model has achieved generalization when it does not over or underfit. Since we want to generalize, we add more parameters to our model for a process called regularization. During the training process, we introduce a penalty to "large coefficients and constrain their magnitudes, thereby preventing a model from becoming overly complex and memorizing the training data instead of learning its underlying patterns" ([GeeksForGeeks](https://www.geeksforgeeks.org/regularization-in-machine-learning/#)). Further, regularization "can help balance the trade-off between model bias (underfitting) and model variance (overfitting) in machine learning, which leads to improved performance" ([GeeksForGeeks](https://www.geeksforgeeks.org/regularization-in-machine-learning/#)).


Regularization often gives us a more robust model. However, the weights of this model might differ from that of a statistical approach, which does not use regularization. 

## Videos
- For a high level overview: [StatsQuest: Logistic Regression](https://www.youtube.com/watch?v=yIYKR4sgzI8)
- [StatsQuest: Logistic Regression Details Pt1: Coefficients](https://www.youtube.com/watch?v=vN5cNN2-HWE)
- [StatsQuest: Logistic Regression Details Pt 2: Maximum Likelihood](https://www.youtube.com/watch?v=BfKanl1aSG0)
- [Odds and Odds Ratio](https://www.youtube.com/watch?v=ARfXDSkQf1Y)

## Further Reading
For the logistic regression recitation, please review the [Logistic Regression chapter](https://christophm.github.io/interpretable-ml-book/logistic.html) from the Interpretable ML book and some of the [Gallery Examples](https://scikit-learn.org/1.5/modules/generated/sklearn.linear_model.LogisticRegression.html#gallery-examples) from sklearn. To look at basic hyperparamter tuning with logistic regression in sklearn, check out [Machine Learning Mastery](https://machinelearningmastery.com/hyperparameters-for-classification-machine-learning-algorithms/).

## Citations
- [Logistic Regression - Interpretable ML Book](https://christophm.github.io/interpretable-ml-book/logistic.html)
- [Logistic Regression - Wikipedia](https://en.wikipedia.org/wiki/Logistic_regression)
- [What is regularization?](https://www.ibm.com/think/topics/regularization#:~:text=Regularization%20is%20a%20set%20of,overfitting%20in%20machine%20learning%20models.)
- [Regularization in Machine Learning](https://www.geeksforgeeks.org/regularization-in-machine-learning/#)
