# Phase-3-Project
An classification analysis that predicts customer churn
## Overview.
Data used is from the Syriatel Customer churn dataset. Our main aim was to predict customer churn and therefore our target variable is the churn column. This makes it a classification regression. There are a number of models used including logistic regression as our baseline model. The model used for prediction was XGB Classifier. The variables that predict churn include Voice mail plan and International plan.
.
## BUSINESS AND DATA UNDERSTANDING.
SyriaTel comapany is a mobile network company located in Damascus, Syria. Over the years, they have noticed that their customers keep leaving. Our main project is to come up with a model that predicts customer churn so that they can prevent such occurences from happening by improving.
It contained 3,333 rows and 21 columns. There were no missing values, we dropped some few columns, the outliers detected seemed reasonable thus retained then did a univariate, bivariate and multivariate analysis of the variables.
## Modelling and Evaluation.
The classification models used in this study include:
1. Logistic regression – we considered logistic regression fit as the baseline model.Had an accuracy score of 86%training, 85%test. The accuracy wasn't bad but we decided to explore more models with hyperparameter tuning.
Hyperparameter tuning is used when you want to improve a model.
• K Nearest Neighbour - it had an accuracy of 91%
• Logistic Regression - We had a slight improvement in accuracy when using hyperparameter tuning as compared to without.
• Gradient Boosting Classifier - had an accuracy of 95%
• Support Vector Classifier - accuracy of 94%
• XGB Classifier - accuracy score of 96%. This had the best accuracy score and performed the best
# ROC CURVE.
The ROC (Receiver Operating Characteristic) curve is a graphical representation used to 
evaluate the performance of a binary classification model.
• The best model was model 5(AUC = 0.88), which was the XGB Classifier model.
• This means that it has the best ability to distinguish between positive and negative classes 
among the models listed. It performs exceptionally well and can be considered the 
strongest model.The model was then used during feature importance.
## FEATURE IMPORTANCE
Feature importance refers to techniques that 
assign scores to input features based on how 
useful they are at predicting a target variable.
From the analysis, the following features had 
the highest importance.
• Voice mail plan
• International plan
• Total night call and night charge
• Total day call and day charge.
## RECOMMENDATIONS.
1) The company should look into the voice mail plan and international plan packages, make 
sure that the people who use these services are well taken care of as they have the 
highest rate of churn.
2) The company could try to either lower its charges per minute for clients, which have 
many call minutes or it could offer flat rates for calls.
3)The company should look for an awarding system or give special offers to their longest 
serving customers to up their spirits.
