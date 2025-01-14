# SHAP (SHapley Additive exPlanations)

## Shapley Values
Shapley values, a game theory method, provide a mechanism to fairly distribute a "payout" to a set of cooperating players. Given a single sample of the dataset, we would like to understand each of its feature values' contribution to the prediction for the sample by explaining the difference between the actual prediction of this given sample and the average prediction for all samples. We can randomly permute the samples to understand the marginal contribution of a feature value to various predictions. The Shapley value is the (weighted) average of marginal contributions. Of course, permutation is expensive computationally.

## SHAP
SHAP (SHapley Additive exPlanations) provides a fast computation of Shapley values for model instabnces. SHAP approximates a Shapley value explanation as an additive feature attribution method via a linear model.

Given the additive nature of SHAP, we not only get individual predictions for each sample, but we can also average the absolute value of all features to get a global feature metric. Further, we can visualize the individual prediction patterns as a beeswarm plot. Moreover, we can use SHAP for partial dependence plots (PDPs) and individual conditional expectation (ICE) plots.


## Citations
- [How Shapley Values Work](https://www.aidancooper.co.uk/how-shapley-values-work/)
- [A Non-Technical Guide to Interpreting SHAP Analyses](https://www.aidancooper.co.uk/a-non-technical-guide-to-interpreting-shap-analyses/?xgtab&)
- [Shapley Values - Interpretable ML](https://christophm.github.io/interpretable-ml-book/shapley.html)  
- [SHAP - Interpretable ML](https://christophm.github.io/interpretable-ml-book/shap.html)
- [An introduction to explainable AI with Shapley values](https://shap.readthedocs.io/en/latest/example_notebooks/overviews/An%20introduction%20to%20explainable%20AI%20with%20Shapley%20values.html#)
- Lundberg, Scott M., and Su-In Lee. “A unified approach to interpreting model predictions.” Advances in Neural Information Processing Systems (2017).
