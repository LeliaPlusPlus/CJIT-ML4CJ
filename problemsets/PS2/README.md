# Developing a Heat Vulnerability Index with Machine Learning

## Introduction
A heat vulnerability index (HVI) is a metric that combines data related to heat, demographics, and sometimes health and the environment. Ideally, the HVI will be correlated to heat-related health outcomes, but health data is often unavailable at relevant scales for privacy reasons. Therefore, some heat vulnerability indices exclude this data. 

HVIs are a relevant policy planning and public health tool to help local officials understand which locations might be most impacted by extreme heat. HVIs highlight vulnerable communities, including by demographic. One potential application of an HVI is to match it with some health outcome to see if it can help local officials respond.

HVIs are usually developed with principal component analysis (PCA), which is an unsupervised method. However, PCA can result in an inconsistent heat vulnerability index. Therefore, we will use SHAP values from our supervised learning model to develop a heat vulnerability index. Since SHAP values are additive, we can develop a heat vulnerability index by summing the SHAP values for our features. We can then use this to understand vulnerability to the urban heat island effect, including through the lens of equity.

## Goal
You are a member of an NIH task force seeking to develop tools for local policymakers that can inform them of their local heat vulnerability. Based on a literature review, you believe a heat vulnerability index could prove useful. 

You gather data from a previous study (Benz and Burney, 2021) and the Climate and Economic Justice and Screening Tool to examine the extent to which environmental factors exacerbate SUHII disparities. The environmental variables include green space (i.e., Normalized Difference Vegetation Index), built-up extent (i.e., Normalized Difference Built-Up Index), and impervious surface (i.e., percent of a tract covered by impervious surface.). The demographic variables include race (Black, Hispanic/Latino, and White) and socioeconomic status (below poverty).

After developing a model and examining your SHAP outputs, you create maps to understand which regions have the most heat vulnerability. In addition, you want to explore how the environment and demographics play a role in heat vulnerability.

## Index Development
Adding SHAP Values
Sum your SHAP values overall, only for environmental factors, and only for demographic factors. Voila! You have a heat vulnerability index.

### Mapping
Create univariate choropleth maps of the SHAP sums. Create a bivariate choropleth map comparing environmental and demographic indices.

### Summary
Summarize the findings for your team. Describe regional patterns in the heat vulnerability index. Discuss how qualitative approaches could complement index development. Discuss whether or not the index would help local officials reach impacted communities.
