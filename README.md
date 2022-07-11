# Predicting The Quality of Vinho Verde Wine Using Physicochemical Factors

![Status Update](https://img.shields.io/badge/Status-Complete-brightgreen) 
![R version](https://img.shields.io/badge/R%20version-4.2.1%2B-lightgrey)
![GitHub repo size](https://img.shields.io/github/repo-size/siyamabu/Life-Expectancy)
![License](https://img.shields.io/badge/License-MIT-green)
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

Badge [source](https://shields.io/)

## Key findings

Alcohol is the most significant predictor of quality wine so interestingly, wines with higher alcohol contents have higher quality. 

## Authors

- [@siyamabu](https://www.github.com/siyamabu)

**Language and Tools:**<br />
* R 🏴‍☠️ 
* R Studio :notebook:
* GitHub :heart_eyes:

**Modules used:**<br />
* vvd
* mass
* ggplot2
* tidyr
* dplyr

**Environments Used:**<br />
* Windows 10 🪟

## Table of Contents

  - [Motivation](#motivation)
  - [Data source](#data-source)
  - [Methods](#methods)
  - [Quick Glance at the Results](#quick-glance-at-the-results)
  - [Lessons Learned and Recommendations](#lessons-learned-and-recommendations)
  - [Limitations and What Can Be Improved](#limitations-and-what-can-be-improved)
  - [Explore the Notebook](#explore-the-notebook)
  - [License](#license)

## Motivation 

## Data Source

- [Vinho Verde Wine Quality](https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009)

## Dataset Description

This dataset contains one categorical response variable (High or Poor) quality wine and 12 physicochemical predictor variables. The 12 physicochemical predictor variables are: Fixed Acidity, Volatile Acidity, Citric Acid, Residual Sugar, Chlorides, Free Sulfur Dioxide, Total Sulfur Dioxide, Density, pH, Sulphates, and Alcohol. The response variable is quality. It was originally ranked on a scale of 1-10 with 1 through 5 being wine of poor quality and 6 through 10 being wine high quality. We changed this to 1 for high quality and 0 for poor quality. There are 1599 wine variants.


## Methods

- Data Characteristics
    * Graphical summaries of the individual variables
    * Transformation of highly skewed variables
    * Scatterplot amtrix
    * Heat map of all the pairwise correlations
- First Order Model With all Predictor Variable
    * Jittered response vs. predicted values with the fitted logistic curve and a lowess fit
    * Residuals vs. fitted value
    * Variance Inflaction Factors, Cook’s distance, and High Leverage
- Model Selection- Stepwise Regression
    * AIC stepwise regression
    * BIC stepwise regression
    * Two-way interaction effects
- Final Model
    * Summary of the parameter estimates, standard errors, and p-values
    * Table of the odds ratios and their confidence intervals
- Model Diagnostics
    * P-values for goodness-of-fit test and likelihood ratio test
    * Deviance residuals vs. fitted values plot
    * Influence diagnostics analysis (Cook’s distance, leverage)
    * ROC plot

## Quick Glance at the Results

Final Model. 

![final model](pictures/final%20model.png)

Scatter Plot of final model. 

![heatmap](pictures/scatter_plot.png)

ROC Plot. 

![graphx](pictures/auc.png)

Residual & Diagnostic Analysis of final model.

![graph1](pictures/residual%20plots.png) 

Jittered Response vs. Predicted Values Plot of final model. 

![graph2](pictures/jittered.png)

Diagnostic Plots of final model. 

![graph3](pictures/diagnostics.png)

Interaction Plot of Log Alcohol and Log Fixed Acidity. 

![graph4](pictures/interaction1.png)

Interaction Plot of Square Root of Volative Acidity and Log Free Sulfur Dioxide.

![graphy](pictures/interaction2.png) 

## Lessons Learned and Recommendations

- Log of Alcohol was the most significant predictor in the final model so interestingly, wines with higher alcohol contents have higher quality. 
- Residual sugar was one of the first predictors removed using stepwise regression. It seems that residual sugar has no significance towards the quality of wine.
- Given that a wine's alcohol percentage is determined during the fermentation process, when sugar is converted to alcohol by yeast a winemaker can opt to prolong that process and produce a higher ABV to potentially increase the perceived quality of their wine. 

## Limitations and What Can Be Improved

- Perceptions of quality are generally subjective. Individuals have different perferences thus, perceptions of quality differ. 
- This analysis only considers physicochemical factors, other factors such as types of grapes used, how long the wine was aged for, location (considering the effects of weather) were not considered. A better model could have been produced and we would have been able to examine the impact of these aforementioned factors to the quality of Vinho Verde wine.
 
## Explore the Notebook

To explore the notebook file [here](https://github.com/siyamabu/Vinho-Verde-Wine/blob/main/vinho_verde_wine.docx)

## License

MIT License

Copyright (c) 2022 Siyabonga Mabuza

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Learn more about [MIT](https://choosealicense.com/licenses/mit/) license

