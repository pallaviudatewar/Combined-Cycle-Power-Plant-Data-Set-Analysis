# Combined-Cycle-Power-Plant-Data-Set-Analysis

## Overview
This report presents a comprehensive analysis of the Combined Cycle Power Plant Data Set, covering the period from 2006 to 2011. The objective is to utilize various machine learning techniques to predict the net hourly electrical energy output (EP) of the plant based on ambient variables such as Temperature (T), Ambient Pressure (AP), Relative Humidity (RH), and Exhaust Vacuum (V).

## Dataset
The dataset contains several years of data from a Combined Cycle Power Plant and includes the following features:
- Temperature (T)
- Exhaust Vacuum (V)
- Ambient Pressure (AP)
- Relative Humidity (RH)

These features serve as the predictors for the target variable:
- Electrical Energy Output (EP)

## Exploratory Data Analysis (EDA)
### Data Structure
- The dataset consists of `9568` rows and `5` columns.
- Each row represents an hourly record of the power plant's operational data.
- Columns correspond to the ambient variables and the net hourly electrical energy output.

### Pairwise Scatterplots
- Scatterplots for all variables against each other, including with the response variable EP, were created.
- The scatterplots revealed relationships and potential correlations between the predictors and the response.

### Descriptive Statistics
- The mean, median, range, quartiles, and interquartile ranges were calculated for each variable.
- A summary table of these descriptive statistics was created to provide an overview of the data distribution.

## Regression Analysis
### Simple Linear Regression
- Simple linear regression models were fitted for each predictor against EP.
- The significance of associations, presence of outliers, and the model fit were evaluated and described.

### Multiple Regression Model
- A multiple regression model using all predictors was developed to predict EP.
- The null hypothesis for each predictor coefficient being zero was tested to identify significant predictors.

## Nonlinear Associations and Interaction Terms
### Polynomial Regression
- Polynomial models were fitted for each predictor to detect nonlinear associations.
- The form `Y = β0 + β1X + β2X^2 + β3X^3 + ε` was used to assess the nonlinearity.

### Interaction Terms
- A full linear regression model including all pairwise interaction terms was run.
- Statistically significant interaction terms were identified and reported.

## Model Improvement
- The regression model was refined by incorporating interaction terms and quadratic nonlinearities.
- Insignificant variables were removed based on p-values, with caution exercised regarding interaction terms.
- Both the refined and initial models were trained on a randomly selected 70% subset of the data and tested on the remaining 30%.
- Training and test mean squared errors (MSEs) were reported for both models.

## KNN Regression
- KNN regression was performed using both normalized and raw features.
- The optimal value of `k` was determined by examining the fit across a range of `k` values from 1 to 100.
- Training and test errors were plotted against `1/k`.

## Comparison of Models
- The KNN regression results were compared with the linear regression model exhibiting the smallest test error.
- An analysis of the results and the performance of the models was provided.

## Conclusion
The findings from this analysis offer insights into the predictive capabilities of linear regression and KNN regression models when applied to the power plant dataset. The report highlights the importance of exploratory data analysis, model selection, and refinement in the predictive modeling process.

