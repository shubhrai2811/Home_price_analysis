---

# Home Price Prediction Analysis

## Project Overview

Welcome to the Home Price Prediction Analysis project! This project explores various regression models to predict home prices using a comprehensive dataset of economic indicators. Our goal is to identify the best-performing models and understand the relationships between different features and home prices.


## Introduction

Predicting home prices accurately is crucial for various stakeholders, including buyers, sellers, and policymakers. In this project, we leverage machine learning models to provide insights into the factors influencing home prices and to achieve high prediction accuracy.

We evaluated six different regression models:
- Random Forest
- Gradient Boosting
- XGBoost
- Linear Regression
- ElasticNet
- Support Vector Regression (SVR)

## Datasets

We had to make use of publically available data to make our own dataset and not use any prebuild datasets.
therefore we found out the most probable factors that affect the house prices in US.
most of the data is downloaded from : https://fred.stlouisfed.org/

The dataset used in this project includes various economic indicators such as:
- Home Prices (CSUSHPISA) : [link](https://fred.stlouisfed.org/series/CSUSHPISA)  (As a proxy to the home prices, S&P CASE-SHILLER Index is used.)
- Per Capita GDP : [link](https://fred.stlouisfed.org/series/A939RX0Q048SBEA)
- Consumer Price Index (CPI) : [link](https://fred.stlouisfed.org/series/CPIAUCSL)
- Working Age Population : [link](https://fred.stlouisfed.org/series/LFWA64TTUSM647S)
- Urban Population : [link](https://data.worldbank.org/indicator/SP.URB.TOTL.IN.ZS?end=2021&locations=US&start=2001)
- Old Age Population : [link](https://fred.stlouisfed.org/series/SPPOP65UPTOZSUSA)
- Unemployment Rate (UNRATE) : [link](https://fred.stlouisfed.org/series/UNRATE)
- Federal Funds Rate (FEDFUNDS) : [link](https://fred.stlouisfed.org/series/FEDFUNDS)
- Employment Rate (EmpRate) : [link](https://fred.stlouisfed.org/series/LREM64TTUSM156S)
- Construction Price Index : [link](https://fred.stlouisfed.org/series/WPUSI012011)
- New houses supply per month : [link](https://fred.stlouisfed.org/series/MSACSR)
- Median Income : [link](https://fred.stlouisfed.org/series/MEHOINUSA672N)
- Total Number of Households : [link](https://fred.stlouisfed.org/series/TTLHH)
- Government Subsidy : [link](https://fred.stlouisfed.org/series/L312051A027NBEA)


## Model Evaluation

We used Mean Squared Error (MSE) and R-squared (R²) values to evaluate the performance of each model. Here's a summary of our findings:

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download.png)

### Random Forest
- **MSE**: 2.17
- **R-squared**: 0.998
- **Insight**: Highest accuracy, explaining 99.8% of the variability in home prices.

### Gradient Boosting
- **MSE**: 3.28
- **R-squared**: 0.997
- **Insight**: Nearly as accurate as Random Forest.

### XGBoost
- **MSE**: 3.46
- **R-squared**: 0.997
- **Insight**: Comparable performance to Gradient Boosting.

### Linear Regression
- **MSE**: 88.5
- **R-squared**: 0.94
- **Insight**: Reasonably accurate but less precise than ensemble methods.

### ElasticNet
- **MSE**: 200.79
- **R-squared**: 0.87
- **Insight**: Lower accuracy, struggles with capturing relationships.

### SVR
- **MSE**: 531.88
- **R-squared**: 0.662
- **Insight**: Poorest accuracy, not suitable for this dataset.

## Results and Insights

### Actual vs. Predicted Home Prices

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download2.png)

The scatter plots show that Random Forest, Gradient Boosting, and XGBoost provide highly accurate predictions, closely matching the actual values. Linear Regression, while reasonably accurate, shows more dispersion. ElasticNet and SVR struggle with higher errors, especially for higher home prices.

### Histograms and Kernel Density Plots

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download3.png)

These plots reveal the distribution patterns of various features:
- Home prices show multiple peaks, indicating variability.
- GDP per capita and other economic indicators have complex distributions, suggesting non-linear relationships with home prices.
- Features like working-age population and urban population show significant impacts on home prices.

### Pair Plot

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download4.png)

Strong positive correlations are observed between material consumption, GDP per capita, CPI, and home prices. Subsidies also show positive correlations with GDP per capita and CPI.

### Time Series Decomposition

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download5.png)

The decomposition shows an upward trend in home prices, regular seasonal patterns, and some variability in residuals towards the end.

### Correlation Heatmap

![image](https://github.com/shubhrai2811/Home_price_analysis/blob/96372ee055434f5a1dc656b7f4d3dc1f56422a36/outputs/download6.png)

The heatmap indicates strong positive correlations between home prices, GDP per capita, CPI, and urban population. Negative correlations include the inverse relationship between the unemployment rate and employment rate.


---

