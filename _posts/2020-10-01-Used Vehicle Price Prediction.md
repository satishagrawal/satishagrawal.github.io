---
title: "Used Vehicle Price Prediction"
date: 2020-10-01
tags:
 - Python
 - Jupyter Notebook
excerpt: "How to come up with a recommended price for an used vehicle based on vehicle condition and other attributes"
header:
  overlay_image: "/assets/usedcarsale.jpg"
  overlay_filter: 0.3 # same as adding an opacity of 0.3 to a black background
  teaser: "/assets/usedcarsale.jpg"
  actions:
    - label: "Go to GitHub Repository"
      url: "https://github.com/satishagrawal/DataScience/tree/main/Used%20Vehicle%20Price%20Prediction"
---
# Predicting a price for a used vehicle

**This notebook illustrates how to train a model that can predict the price for a used vehicle given all the attributes**

The price of the new vehicle is determined by the manufacturer. The manufacturer considers a variety of factors including government taxes, used raw materials cost, the labor involved, intended profit margin per unit, and many other factors that may contribute to the price of the car to come up with the Manufacturer Suggested Retail Price (MSRP). So, buyers of new cars are a bit more confident about the price of new cars; which is not always true with the price of an old car. The used car buying is a very complex process, as an average buyer might not think of all the variables affecting or involved in the price of the vehicle. Car sellers seldom take advantage of such a scenario by listing unfair prices owing to the demand. On the seller's part also it's quite hard to estimate the used car price manually. Generally, experienced sellers can think of some of the parameters like mileage on the vehicle, condition of the vehicle, fuel type, and vehicle age, etc. However, for experienced sellers also, it is hard to consider all parameters while estimating used vehicle price. So, there is a necessity for a used vehicle price prediction system to reliably determine the fair price of the vehicle using various vehicle parameters. There are existing models in the market that estimate the used vehicle price; we are not confident about the accuracy and the quality of the existing models. Depending on the organization that developed these models, those may have biases to benefit the seller. This project aims to train models for the data set chosen. The data set is one from Craigslist used car listings. We are expecting it to be generalized to the rest of the world and other listing portals.

## Method

We chose a data set from Kaggle @ https://www.kaggle.com/austinreese/craigslist-carstrucks-data. This data set has more than 450k records and 25 attributes for each record. We are training a supervised learning model; the target variable is the “price” of the vehicle. We have split our data into the training set and test set to avoid test data getting used in imputation and training. We are dropping a few columns from the start before starting any analysis considering those may not correlate as much (or at all) to contribute to the price of the used vehicle. We dropped unique listing id, image URL, listing URL, region URL, VIN, and description of the car. These columns do not have a direct correlation with the target variable. As part of the data cleansing process, we looked at the distribution of the listing year column. We removed records located outside of the United States by latitude and longitude. We restricted records only from latitude between 25 and 50, and longitude between -125 to -65. We dropped records with extreme values for the year column with a value less than 1995 and more than 2020. We also removed the outliers from the dataset based on the odometer readings and the final price. We removed records with odometer readings of more than 170,000 miles. For removing records by price, we decided to remove records with a price outside of the range of $2000 to $60,000. As part of feature engineering, we have added a new column for the age of the car at the time of listing. The value for the age in the month is derived from the model year and the date of listing. For the model year month, we considered September of the previous year of the model year as most of the car manufacturers launch their next year's car models in August/September of the current year. We found that the distribution of the age for the data set is a right-skewed distribution with a single peak.

## Author

**Satish Agrawal**
