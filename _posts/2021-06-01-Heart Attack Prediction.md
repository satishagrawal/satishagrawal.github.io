---
title: "Heart Attack Prediction Model"
date: 2021-06-01
tags:
 - Python
 - Jupyter Notebook
excerpt: "Train a prediction model to predict the risk of heart attack"
header:
  overlay_image: "/assets/SparkAggBackground.png"
  overlay_filter: 0.3 # same as adding an opacity of 0.3 to a black background
  teaser: "/assets/heartattack.png"
  actions:
    - label: "Go to GitHub Repository"
      url: "https://github.com/satishagrawal/DataScience/tree/main/Heart%20Attack%20Prediction"
---

# Train a prediction model to predict the risk of heart attack

**This notebook loads the data set, performs EDA, cleans the data up and trains a few models using exhaustive train techniques to predict if patient risk of heart attack.**

## The Data
The data set has several observations of patients records and the outcome if patient had a heart attack. This data set is pulled from kaggle @ https://www.kaggle.com/kumudadk/heart-attack-prediction-and-analysis?select=heart.csv

## Method
I chose a data set from Kaggle @ https://www.kaggle.com/kumudadk/heart-attack-prediction-and-analysis?select=heart.csv. This is a small dataset with under 500 observations and fourteen different attributes showing health condition of patients and the outcome if patient had an attack. I trained a supervised learning model; the target variable is the “output” variable which indicates if patient had an attack or not. I used regression algorithms to train a predictive model. I first split the data into the training set and test set to avoid test data getting used in imputation and training. I dropped a few columns from the start before starting any analysis considering those were not correlated as much (or at all) to contribute to the output. And then here onwards I started working on train set only which contains the 80% of the available observations. The first step I took was to observe each and every attribute in the set. As part of data cleansing process, I looked at the distribution of the variables. Some of the variables indicated the outliers and missing values which I handled as many of the machine learning algorithms do not handle missing values. Diagram above shows the distribution of age in the data set. Age plays an important role in determining if patient is prone to the disease. The distribution of the age data looks close to normal and do not require any preprocessing. Similarly, below diagram shows the count plot of chest pain types. There are four categories in the set for chest pain. Chest pain is already encoded in the scale of 0-3 which means:

0 = Typical Angina,
1 = Atypical Angina,
2 = Non-anginal Pain,
3 = Asymptomatic

I did similar analysis on all of the other attributes in the dataset and did transformations as needed. Next, I generated a correlation matrix of all the attributes which indicated a strong correlation of output with the chest pain, slope and maximum heart rate achieved.
Once I had the processed data set at hand, I started training regression models. I trained KNeighborsClassifier, LogisticRegression, DecisionTreeClassifier and SVC models. I used GridSearchCV to do exhaustive training and hyperparameter tuning. I used k fold stratified cross validation to make sure every split had the same proportion of true and false output values and equal representation of both output classes. I ended of 70 different models and compared those against each other’s using accuracy score as the comparison metric. I decided to use R-square as a scoring metric. The most common interpretation of r-squared is how well the regression model fits the observed data.


## Author
**Satish Agrawal**
