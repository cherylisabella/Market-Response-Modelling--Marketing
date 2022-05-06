# Market Response Modelling--Marketing
Marketing and business analytics;   Market Response Modeling for a telecommunication provider 
Github page link: https://cherylisabella.github.io/Market-Response-Modelling--Marketing/

This project aims to use market reponse modelling to develop the right marketing mix for a hypothetical telecommunications provider.
In this scenario, the telecommunications provider currently uses traditional advertising (mainly TV) and Facebook to market its subscriptions.

Here is the brief structure of this repository:

# Data 
This project will analyse how effective the current channels are in acquiring new customers. Therefore, the following data were collected:

    number of newly acquired customers across 118 weeks
    the investment in traditional advertising
    the number of impressions of Facebook posts initiated by the telecommunications provider
    information about media and buzz events, holiday periods, promotions
    marketing buzz about the telecommunications provider on Twitter.

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

# Dynamic effects
The analysis of the dynamic effects in this project can be found on the associated Github page or .rmd file.

# Influence of traditional advertising on acquisition
The analysis of the inifluence of traditional advertising on acquisition can be found on the associated Github page or .rmd file.

# Influence of FB impressions on acquisition
The analysis of the influence of Facebook impressions on acquisition can be found on the associated Github page or .rmd file.

# Conclusion
The conclusion and recommendations for the telecommunications provider can be found on the associated Github page or .rmd file.
