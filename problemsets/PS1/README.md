# Urban Heat Island Disparities

## Introduction
Urban areas experience higher temperatures than their rural counterparts, which is referred to as the urban heat island (UHI) effect (Oke, 1982). Urbanization alters land cover, replacing natural landscapes with impervious surfaces (Grimmond, 2007). For example, parking lots and roadways constructed with asphalt and concrete may replace trees and other vegetation. However, impervious surfaces have low land surface albedo, so they absorb more energy from solar radiation and re-emit it as heat (Mohajerani, Bakaric, and Jeffrey-Bailey, 2017). In contrast, natural surfaces, such as vegetation and water bodies, reflect solar radiation, shade man made surfaces, and release moisture, which can cool the local microclimate. Moreover, building infrastructure, vehicles, and local industry generate heat and greenhouse gas emissions, contributing to the UHI effect (U.S. Global Change Research Program, 2017). As a result, the UHI effect can be more pronounced in more densely populated areas (U.S. Global Change Research Program, 2017). Concerningly, the UHI effect is expected to exacerbate as urban areas continue to expand in area and population and modify land cover (U.S. Global Change Research Program, 2017), impacting at least 83 percent of the US population (World Bank, 2023). In general, increasing heat stress as a result of climate change leaves urban residents vulnerable to a myriad of hazardous health outcomes, including heat stroke, hospitalization, and mortality. In fact, heat mortality is the leading cause of weather-related death, and it is an increasing concern in U.S. cities due to climate change (Lo et al., 2019). 

Emerging research demonstrates that across the United States marginalized groups overwhelmingly face higher burdens of heat stress, exacerbated by the built environment, with respect to the distributions of the urban heat island effect and intra-urban heat. One study of UHIs in 175 contiguous U.S. cities found that in 169 cities, or 96.5% of the studied cities, people of color on average reside in census tracts with a greater surface urban heat island intensity (SUHII) (Hsu et al., 2021). In addition, the study found that on average those below the federal poverty line live in higher places with greater SUHII intensity compared to those above twice the poverty line (Hsu et al., 2021). Furthermore, researchers have sought to examine the extent to which the built environment plays a role in SUHII intensity disparities. A study, representing 300 million people living in U.S. urban areas, found that low-income and less educated tracts face higher surface heat than their more affluent and educated counterparts; in addition, Black, Hispanic, and Asian communities experience higher SUHI intensity than non-Hispanic white communities, even after controlling for income (Benz and Burney, 2021). These widespread differences occurred due to greater built-up intensity, less vegetation, and to a smaller degree population density (Benz and Burney, 2021). Moreover, a large-scale study on intra-urban heat in 108 historically redlined cities found that in 94 percent of cities, redlined areas possessed higher land surface temperatures than their non-redlined counterparts, coinciding with lower percentages of tree canopy in redlined area (Hoffman, Shandas, and Pendleton, 2020). Nationally, redlined areas experienced 2.6 degrees Celsius higher land surface temperatures on average (Hoffman, Shandas, and Pendleton, 2020). Further, a study, accounting for 167 million people in urban areas, found that urban temperature disparities co-occur with tree cover differences (McDonald, 2021). That is, low income census blocks in urban areas have fewer trees and warmer microclimates (McDonald, 2021). The average low-income block contained 15.2 percent fewer trees while being 1.5⁰C warmer compared to blocks with higher income (McDonald, 2021). 

## Goal
You are a quantitative analyst at the White House Council on Environmental Quality. Your team is currently working on a project about urban heat island disparities nationally. Your supervisor has asked you to study the environmental factors that contribute to SUHI disparities in marginalized communities. You suggest a machine learning approach. Machine learning enables us to develop a non-linear, non-parametric, and interpretable model, which helps us to compare several continuous variables at once. Given the continuous and non-linear nature of environmental and SUHII data, this approach comes in handy for your analysis. 

You gather data from a previous study (Benz and Burney, 2021) and the Climate and Economic Justice and Screening Tool to examine the extent to which environmental factors exacerbate SUHII disparities. The environmental variables include green space (i.e., Normalized Difference Vegetation Index), built-up extent (i.e., Normalized Difference Built-Up Index), and impervious surface (i.e., percent of a tract covered by impervious surface.). The demographic variables include race (Black, Hispanic/Latino, and White) and socioeconomic status (below poverty).

After gathering the data, it is your job to perform data exploration and model development. Your data exploration includes descriptive statistics, histograms, scatter plots, correlation analysis. Your model development focuses on developing a tree-based model and gaining insights through SHAP values. Lastly, you will summarize findings for your team.

## Data Exploration
### Spearman Correlation Analysis
How does race and poverty correlate with environmental factors and SUHII? Which variables are most correlated with SUHII? How does this compare to the research discussed in the introduction? Describe any other interesting correlations.

### Histograms
What do the distributions reveal about race, socioeconomic status, environmental factors, and SUHII? How does this compare to the research discussed in the introduction?

### Scatter Plots
Create scatter plots to visualize the relationships between demographic and environmental factors, using urban heat island intensity as a heatmap.

## Model Development
### Model Performance
RMSE is the standard deviation of the residuals. Based on the RMSE, how did the model perform? Based on the R2, how well did the model fit the data? How does model performance impact your communication of the model to your team? 

### Predictive Factors of Urban Heat
Using the SHAP values, discuss the most predictive factors of urban heat intensity. Why do you think these are the most predictive factors? How does this compare to the previous research discussed in the introduction? 

### Multi-Dimensional Analysis
Using SHAP scatter plots, discuss how racial composition of a tract and environmental factors impact SUHII (i.e., use environmental factors as a heat map by race). Do the same for poverty status and environmental factors. Explain the disparities that these plots illuminate. How does this compare to the previous research discussed in the introduction? 

### Summary
Summarize the findings for your team. Based on your analysis, how do environmental disparities by race and socioeconomic status influence SUHII? 

