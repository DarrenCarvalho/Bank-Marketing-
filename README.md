# Bank Marketing

Classify whether a client will subscribe to term deposit plan (Binary Classification).

## Data set url: 

https://www.kaggle.com/henriqueyamahata/bank-marketing


## Features:

* Discrete = pdays, previous, emp.var.rate, cons.price.idx, cons.conf.idx, nr.employeed.
* Continuous = age, duration, campaign, euribor3m.
* Dichotomous = default, housing, loan, contact.
* Polychotomous = job, marital, education, month, day_of_week, poutcome.

## Pre-processing

* Missing Values in numerical variables are labelled “999” and in categorical variables they are labelled “unknown”.
* Default and pdays had 20.2 and 96.32 percent missing values respectively and hence were dropped from the data frame.
* Rest of the rows with missing values were dropped. (Since the dataset was highly imbalanced).

## Exploratory Data Analysis

* Highly Imbalanced dataset ( 9:1 ).
* Duration among the yes and no class, Clients who have agreed for a term deposit plan tend to have a larger duration of   conversation. Probably to get to know more about the details of the term deposit plan. On the other hand, the clients who are not interested do not attend the call for a long duration. 
* Campaign vs Target : the number of campaigns held among both the classes seem to be relatively same but since the data set is imbalanced, the peaks deviate. 
* Month vs Target : Most Employees have been contacted in May followed by July, August and then June. The percent of people agreeing to a Term deposit plan are also significantly large as compared in other months.

## Feature Engineering
* Feature Creation:
  * Age Binning ( Based on the quartiles ).
  * Principle component analysis.
* Encoding
  * Dichotomous Variables (1, 0)
  * Polychotomous  Variables (Label Encoding, One Hot encoding)
* Up sampling using SMOTE

## Models:
* With Hyperparameter Tuning:
  * Random Forest Classifier
  * XGBoost Classifier
* Upsampling with One Hot Encoding and Label Encoding:
  * CatBoost Classifier
  * LightGBM Classifier
* Voting Classifier:
	* Logistic Regression
	* KNN Classifier
	* Decision Tree Classifier.

