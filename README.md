# Analysis of the income pattern in US census data

Full Analysis : [Notebook](https://github.com/pantonar/income_census/blob/main/Technical%20assessment.ipynb)

The purpose of this analysis is to identify the charactersitics associated with individuals earning more than $50,000. I then develop a model predicting income class based on the census data.

## Exploratory analysis
* 25% of the sample are children
* no missing values
* most of the features are categorical (33 vs only 7 continuous)
* the variables correlating most with the income category are weeks_worked, company size, age and capital gains

## Data preparation
* one-hot encoding of categorical variables
* normalisation


## Feature selection
* correlation > 0.05

## Models
### Performance Analysis
![](/png/metrics_table.png?raw=true)
### ROC Curve of Top 5 Models
![](/png/roc.png?raw=true)
