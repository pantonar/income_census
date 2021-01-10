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
I train 5 different models. For each of them, I undertake a hyperparameter search, and detail below the best performing parameters on the CV set (20% of the train set):
* Random Forest: 
  * the best parameters are: a forest of 300 trees with maximal depth 50, all features included in split operatedd in 20% of the sample
* Adaboost:
 * 500 estimators
* Logistic regression:
 * L2 penalty with regularisation weight of 1
* K-Nearest Neighbours:
 * based on the 5 neareast neighbours with uniform weights
* Neural Network:
 * Logitic activation function and 4 hidden layers of sizes (20, 10, 5, 2)
### Performance Analysis
The Random Forest model is the best able to estimate the individual's income category. It outperforms all other competing models, with an overal accuracy of 95.6% on the test set, and error rate of 4.4%.


![](/png/metrics_table.png?raw=true)
### ROC Curve of Top 5 Models
![](/png/roc.png?raw=true)

## Challenges and future developments
