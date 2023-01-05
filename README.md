# SyriaTel Customer Churn Analysis

Author: Simran Kaur

## Problem

SyriaTel is a telecommunications company in Syria. They have been informed that some of their customers have started to churn, aka, discontinue their service. Syriatel wants to understand what are some indicators that a customer will ("soon") discontinue their service.

This analysis uses logistic models to determine what is causing customers to churn and possible preventative measures that taken. 

## Data 

The dataset was taken from kaggle.com. It contains 3,333 records and has information on clients' accounts with SyriaTel. This includes minutes they have used, how many day/evening/international calls have been made, the number of times a customer has called customer service and if the customer has churned. 

## Methods

The first step in the process was EDA. 
* Features were seperated into continuous and categorical categories. 
    * Distribution plots, pairplots and a correlation heatmap were plotted for the numerical features.
    * Countplots were plotted for the categorical features
* Outliers past three standard deviations were dropped.
* Highly correlated features 0.9 or greater were dropped. 
* One-hot encoding was performed on the categorical features.
* Numerical features were scaled.
* A countplot was plotted for churn, which is the independent variable. A class imbalance was discovered and SMOTE was applied to resolve the issue. 

The second step in the process was the modeling. 
* A logistic regression classifier was ran and it served as the baseline model. 
* A random forest classifier was ran. 
* A decision tree classifier was ran. 
* The random forest model had the best accuracy and F1 score. 
* Hypertuning was performed on the random forest model and it yeilded simialr results as the original model ran.

## Results

Three different machine learning models have been used to predict "churn" feature from the dataset and the models were compared using F1 Score, precision, recall, accuracy and AUC (Area Under Curve - ROC Curve) performance metrics to choose the best model.In terms of accuracy, the according to F1 score and AUC metrics, the Random Forest Classifier model has performed the best amongst all the models ran.

Hyperparameter tuning was performed to determine what parameters would yield the best model result. Another random forest regression was ran and it yielded a very similar accuracy and F1 score. The second model had a higher recall and lower precision. Either or random forest model would be good to use.

## Suggestions

SyriaTel should start focusing on strategies that will prevent customers from churning as they have already lost 14.8% of their customers. Some ideas are:
1. Offering a discount to customers who have made more than 2 phone calls within 6 months. This small incentive will help accomodate the customer for the issues they have been facing and in turn, lower churn.
2. Starting an internal forum where customer service representatives document the common reasons customer call Syriatel. This way the company can start implementing strategic solutions to resolve those issues.
3. Starting a rewards program. The initiative can be called SyriaTel Sundays and every week, the company can offer some sort of discount in partnership with another vendor. This small step will excite customers and want to continue their service with Syriatel.

## Further Information

See the full analysis in the Jupyter Notebook or review this presentation.

For additional information, contact Simran Kaur at simran.kaur@flatironschool.com

## Repository Structure
```
├── images
│   ├── best_parameters.jpeg
├── notebook.ipynb
├── dataset.csv
├── presentation3.pdf
└── README.md