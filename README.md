
Phase-3-Project
A classification analysis that predicts customer churn.
## INTRODUCTION.
Customer Churn - the natural business cycle of losing and acquiring customers. Every company, no matter the quality of their product experience customer churn. <br>Churn rate - is the percentage of subscribers who cancel their subscriptions to a service during a specific time period.For a company to achieve profits, its rate of acquiring new customers must be greater than its turnover rate.

## Overview.
Data used is from the Syriatel Customer churn dataset. Our main aim was to predict customer churn and therefore our target variable is the churn column. This makes it a classification regression. There are a number of models used including logistic regression as our baseline model. The model used for prediction was XGB Classifier. The variables that predict churn include Voice mail plan and International plan.
.
## BUSINESS AND DATA UNDERSTANDING.
SyriaTel comapany is a mobile network company located in Damascus, Syria. Over the years, they have noticed that their customers keep leaving. Our main project is to come up with a model that predicts customer churn so that they can prevent such occurences from happening by improving.
It contained 3,333 rows and 21 columns. There were no missing values, we dropped some few columns, the outliers detected seemed reasonable thus retained then did a univariate, bivariate and multivariate analysis of the variables.
## DATA UNDERSTANDING.
Dataset Description:
The dataset comprises the following features:

1.State: The state in which the customer resides (categorical).

2.Account Length: Number of days the customer has been with SyriaTel (numerical).

3.Area Code: Three-digit area code of the customer's phone number (categorical).

4.Phone Number: Unique identifier for each customer (string).

5.International Plan: Whether the customer has an international calling plan (binary: "yes" or "no").

6.Voice Mail Plan: Whether the customer has a voicemail plan (binary: "yes" or "no").

7.Number Vmail Messages: Number of voicemail messages received by the customer (numerical).

8.Total Day Minutes: Total minutes of daytime calls (numerical).

9.Total Day Calls: Total number of daytime calls made by the customer (numerical).

10.Total Day Charge: Total charges for daytime calls (numerical).

11.Total Eve Minutes: Total minutes of evening calls (numerical).

12.Total Eve Calls: Total number of evening calls made by the customer (numerical).

13.Total Eve Charge: Total charges for evening calls (numerical).

14.Total Night Minutes: Total minutes of nighttime calls (numerical).

15.Total Night Calls: Total number of nighttime calls made by the customer (numerical).

16.Total Night Charge: Total charges for nighttime calls (numerical).

17.Total Intl Minutes: Total minutes of international calls (numerical).

18.Total Intl Calls: Total number of international calls made by the customer (numerical).

19.Total Intl Charge: Total charges for international calls (numerical).

20.Customer Service Calls: Number of customer service calls made by the customer (numerical).

21.Churn: Target variable indicating whether the customer churned ("True" or "False").
## PROBLEM STATEMENT.
SyriaTel faces high loses due to current high customer churn rate. The primary challenge is the lack of an effective method to predict customer churn so as to prevent it before it happens thus reducing churn rate and customer satisfaction. The company aims to leverage on its historical data and machine learning techniques to develop a predictive model that predicts customer churn ahead of time.
## OBJECTIVES.
Main Objective: To come up with a classification machine learning model that accurately predicts customer churn for SyriaTel.
## Specific Objectives.
i) Identify the key factors that lead to customer churn.<br>
ii) Come up with a a good model to predict customer churn<br>
iii) Give recommendations on how to retain customers based on the information collected.

## UNIVARIATE ANALYSIS.
# i) What percentage of customers end up leaving?
![HU](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/a1601e1c-189a-42eb-953f-d5b8854c1200)<br>

About 14.5% of SyrialTel customers decide to cancel their subscription with the company.
# ii) How many people are on the International plan?
![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/b30cfb80-e5aa-42cd-802b-1e053261dcc7)

Most customers do not go for the international plan.
An analysis of the international plan against churn could give us an analysis of how good the plan is.

![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/48c53405-3b22-4bb5-90dd-23c2b8e81f59)
The number of calls keep decreasing, but 7 calls to customer care is alarming, lets look into that.

## 2. BiVariate Analysis
i) Does an increase in Customer service call lead to a higher churn rate?
![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/2d895093-48ae-4c30-9ca3-1f179b5d7c0c)

Yes. An increase in number of customer service calls generally leads to an increase in churn rate. The company should address any concerns raised by a customer during this calls immediately. In addition, the company can also look into making sure that the customer service department knows how to handle customers professionally.

ii) How many people on the international plan end up leaving?

![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/5841be82-8c43-4836-adc3-408c04128ee3)

Majority of the people on the international plan end up leaving. This could be an indication of poor service.

iii)How many people on the Voice mail plan end up leaving?

![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/4e4154de-e077-4b41-9a3b-dcecce5c9d8a)

Some people with the voice mail plan end up leaving. May need some improving

## Multivariate Analysis.
Multivariate analysis involves exploring relationships and patterns between multiple variables in a dataset. This process helps uncover insights, correlations, and dependencies that can inform further analysis or modeling.

![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/8a908fbe-97a3-4d48-a1f4-ece989dda295)

## COLINEARITY AND MULTICOLINEARITY
Checking for collinearity between dependent and independent variables

![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/012fff3a-1dfd-40d6-97d1-77a02ca30aed)

From the analysis, Customer service calls has the correlation with Churn

Checking for Multicolinearity
High correlation,(e.g above 0.7)indicates multicollinearity. If the VIF is greater than 5 or 10, it indicates multicolinearity. Higher VIF signify stronger correlation with other predictors.
Some of the columns were dropped due to multicolinearity.

## DATA PREPROCESSING.
The following are steps taken during data preproccesing.
  Identify the X and Y variables.
  Perform a train test split.
  Encode your categorical variables.
  Scale your data.
  Fit the models.
BASELINE MODEL.
Logistic regression was used as our baseline regression. The training accuracy was 86% and test accuracy was 85%. As a base model, this isn't bad. Lets try introduce other models  and hyperparameter tune them.

Models used and their accuracy.
  Logistic regression - 86%.
  KNN Classifier - 91%.
  Gradient Boosting Classifier - 95%.
  Support Vector Classifier - 94%
  XGB Classifier - 96%.
From the above analysis, XGB Classifier has the best accuracy.

## ROC Curve.
In ROC Curve, we plotted all the models in one axis to evaluate their respective AUC scores.
![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/0b9aa7fa-4176-4144-a21b-c4f8249d642b)

The ROC (Receiver Operating Characteristic) curve is a graphical representation used to 
evaluate the performance of a binary classification model.
• From the above analysis, we see that the best model was model 5(AUC = 0.88), which 
was the XGB Classifier model.
• This means that it has the best ability to distinguish between positive and negative classes 
among the models listed. It performs exceptionally well and can be considered the 
strongest model.

## FEATURE IMPORTANCE.
Feature importance refers to techniques that assign scores to input features based on how useful they are at predicting a target variable.
![image](https://github.com/kananamuthomi/Phase-3-Project/assets/151963471/5f85cac6-77c1-4f2d-a438-3ee35d36c68c)

From the analysis, the following features had the highest importance.
• Voice mail plan<br>
• International plan<br>
• Total night call and night charge<br>
• Total day call and day charge.<br

i) What Key factors lead to customer churn?.
Voice mail plan and International plan had the highest importance, suggesting that these two features have the highest influence in predicting churn. Total international minutes and total international calls have no importance indicating that they do not contribute to the models ability to predict churn.

## RECCOMMENDATIONS.
1) The company should look into the voice mail plan and international plan packages, make sure that the people who use these services are well taken care of as they have the highest rate of churn.<br>

2) The company could try to either lower its charges per minute for clients, which have many call minutes or it could offer flat rates for calls<br>

3) The company should look for an awarding system or give special offers to their longest serving customers to up their spirits


    






