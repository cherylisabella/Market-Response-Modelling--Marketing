# Marketing -- Market Response Modelling
Marketing and business analytics;   Market Response Modeling for a telecommunication provider.

Github page link: https://cherylisabella.github.io/Market-Response-Modelling--Marketing/


This project aims to use market reponse modelling to develop the right marketing mix for a hypothetical telecommunications provider.
In this scenario, the telecommunications provider currently uses traditional advertising (mainly TV) and Facebook to market its subscriptions.

Here is the brief structure of this repository:

# Data 
This project will analyse how effective the current channels are in acquiring new customers. Therefore, the following data were collected:

- number of newly acquired customers across 118 weeks
- the investment in traditional advertising
- number of impressions of Facebook posts initiated by the telecommunications provider
- information about media and buzz events, holiday periods, promotions
- marketing buzz about the telecommunications provider on Twitter.

The variables and their descriptions are shown below:

![](mrm%20variables.png)

# Categorisation
The first approach is to categorise all variables in the form of a market response framework. 

![](market%20response%20framework.png)

# Linear Regression Analysis
The data has been cleaned prior to its upload into R. Therefore, we can
proceed with a linear regression analysis on the data.

- All of the variables are numeric. 
- Since all of the variables have different ranges, the min-max standardisation is used so that each variable's values are between 0 and 1.

![](mrm%20model%20results.png)

## Regression model performance

The performance of the linear regression model will be evaluated in 3
ways:

1.  Model Assumptions
2.  Model fit
3.  Significance of coefficients (via T-tests)

### Model Assumptions

The analysis of the model assumptions can be found on the associated Github page or .rmd file.
Results:

- Linearity of the data: A linear relationship between the predictors and outcome variables can be assumed as the Residuals vs Fitted plot shows no fitted pattern, and the red line is approximately horizontal at zero.
- Homoscedasticity: residuals can be assumed to have a constant variance since the residuals in the Scale-Location plot are spread rather equally along the ranges of predictors.
- Independence: can be assumed between and within the customers since each customer is a unique individual (ratings by an individual customer are not expected to be dependent on ratings by other customer(s)).
- Normality: can be assumed since the normal probability plot of residuals approximately follow a straight line.
- Metric scale: all variables are on the metric scale.

Model Fit

- The adjusted R-Squared is only 0.3857 meaning that only approximately 38.6% of the variance of the dependent variable is explained by the model ⇒ This suggests that this model is not a good fit.
- The p-value associated to the F-statistic is < 0.05 ⇒ this means at least 1 independent variable is significantly related to Acquisition.
- The F-statistic of 10.18 is relatively small given the size of our data.
- The model has an RSME of 0.314 which is relatively good as there is little variation in the spread of data.

![](mrm%20coefficients.png)

Significance of coefficients (via T-tests)
- Before evaluating the significance of coefficients, I did a two-fold cross validation and split the dataset into a training subgroup with 88 observations and a test set with 30 observations.
- The two-sample T-test for difference in means was used to validate the partitions as the dataset is entirely numerical.

Derivation of coefficients can be found in the associated .rmd file

# Dynamic effects
- The effort put into marketing sometimes influences sales in future periods. This is known as the carryover effect.
- One type of carryover effect is the delayed-response effect. Some of the variables (e.g., traditional advertising and Twitter volume) are delayed by one week. This has - been done to account for the delayed effect this action might have on acquisition.
- This model takes into account some dynamic effects that are relevant to this case.
- However, the inclusion of information from past observations of a series does not necessarily include other omitted variables that may explain some of the historical variations, and that may lead to more accurate forecasts.

# Influence of traditional advertising on acquisition
- The coefficient for traditional advertising is 0.297 (3sf). This means that traditional advertising and acquiring new customers are positively correlated.
- That is, when traditional gross media expenditures increase, the number of newly acquired customers is likely to increase.
- Note: 0.297 is a proportional effect.


# Influence of FB impressions on acquisition
- The coefficient for Facebook impressions is 0.084, which indicates that like traditional advertising, Facebook impressions and acquiring new customers are positively correlated, albeit to a relatively smaller extent.
- This means that increasing number of impressions on Facebook will likely lead to increase in the number of newly acquired customers.


# Conclusion

![](mrm%20conclusion.png)

Results:
- The model indicated that the most effective communication channel is Twitter as it has the highest coefficient.
- The difference between the most effective and second most effective communication channel - traditional advertising - is relatively small. However, the difference between Facebook, which turns out to be least effective, and traditional advertising is fairly large.
- The influence of Twitter is more than three times as large as the influence of Facebook impressions. This insight is useful for the company to decide on how to divide their resources.
- It is surprising that traditional advertising is remains impactful in this day and age.
- It can be concluded that digital advertisings’ impact is higher when coupled with traditional advertising, because they need the credibility traditional advertising provides.

Recommendations for telecommunication provider
- As seen from the quantitative evaluation of coefficients, the use of more modern advertising, notably Twitter, is recommended for the telecommunication provider . This “digital first” approach would be a more holistic marketing communication campaign as it meet the changing consumer landscape of tech savvy consumers.
- Further, the telecommunication provider could consider reaching prospective consumers through personal communication channels (eg face-to-face pitches) and buzz marketing to capitalise on word-of-mouth influence for higher acquisition and profits.
- Lastly, the firm should also evaluate the return on advertising investment through the sales and profits effects. This can be done by comparing past sales and profits with past advertising expenditures, or through experiments(eg varying the amount it spends on advertising in different market areas and measuring the differences in the resulting sales/acquisition and profit levels.
