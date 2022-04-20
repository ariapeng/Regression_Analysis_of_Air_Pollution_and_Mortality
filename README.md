# Regression_Analysis_of_Air_Pollution_and_Mortality
Multiple linear regression analysis of air pollution an mortality using SAS

The objective of this project is to seek to find the association between air pollution and mortality as well as to obtain a prediction equation for mortality as a function of the predictor variables. The dataset used is collected from 57 US cities.

We follow the PISEAS (Planning, Investigating, Specification, Estimation, Assess, and Selection) rule, a general system for performing a regression analysis except for 'P' since the data is designated here. MLR
(multiple linear regression) is started with the most common OLS (ordinary least square) model. After investigation of the data, an increased power transformation on y is conducted based on Box-Cox test and estimate parameters are then obtained for specification of the fitted model. However, MSE (mean squared error) and R^2_Adj of the model are not desirable. Also, adequacy checking using diagnostic measures indicate the assumptions on error term do not hold well. To improve the fit, possible outliers and influential points are identified by influential analyses. After removing one outlier, the model is refitted, making the assumptions on error term hold while MSE and R^2_Adj do not improve much. Another transformation on y did not help much, likewise. Hence, we conclude that OLS model does not perform well on the data.

Since a model is supposed to be as informative as possible, deleting an outlier is not preferred or recommended. We try to accommodate it, such as downweighting it to a less impactful point, or almost to zero,
by using WLS (weighted least square) model. Thus, the WLS model is fitted instead of the OLS one. To our delight, MSE, R^2_Adj and even CV (coefficient variance) improved significantly with all observations kept.

Finally, variable selection measures were performed to obtain the optimal model.
We conclude Mortality is positively associated with mean annual precipitation, percentage of the population that is nonwhite, relative pollution potential of sulfur dioxide, and is negatively related to relative pollution
potential of oxides of nitrogen.

Fortunately, multicollinearity was not observed throughout the whole regression analysis.
