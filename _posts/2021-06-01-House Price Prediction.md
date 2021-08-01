---
title: "House Price Prediction Model"
date: 2021-06-01
tags:
 - Python
 - Jupyter Notebook
 - Predictive model
 - Regression
 - Supervised learning
excerpt: "Predict a fair market price for a house"
header:
  overlay_image: "/assets/HouseForSale.jpg"
  overlay_filter: 0.3 # same as adding an opacity of 0.3 to a black background
  teaser: "/assets/HouseForSale.jpg"
  actions:
    - label: "Go to GitHub Repository"
      url: "https://github.com/satishagrawal/DataScience/tree/main/House%20Price%20Prediction"
---
# House Prices Prediction using Regression
**This analysis takes the real state transactions for a few last years and trains a regression model to accurately predict the price of a house**

## The Data
For this project, I have selected a dataset from Kaggle [Kaggle data set]. This data set has 81 different attributes about houses sold recently, which includes the sale price. As I am working to train a model that can predict the sale price, that is the target variable for this project. The sales price is a continuous number in US dollars.
All other 80 variables are explanatory variables that help determine the sales price. Below is the list of main variables in the data set:

1.	Basement information: There are around nine attributes defining the condition and the quality of the basement in the house. The condition of the basement is an important factor which impacts the final price and the valuation of the house. Few attributes are: is basement finished? What is the square footage of finished area? Is it a walkout basement? Etc.

2.	Garage information: There are at least seven attributes about the condition of garage(s) in the house. Garage also play a vital role in the house price. For example, house with three car garages is going to be more expensive than two or one car garage.

3.	Lot information: There are a few attributes that have the information around the lot for example, lot size, lot shape, lot frontage etc. Lot details is one of the many important attributes that determine the house price.

4.	Year built: This is when the house construction was finished. Older house may have older appliances and may have other issues. Year build is a key to help determine the house price.

5.	There are quite a few important attributes that impact the final price of the house for example, number of bathrooms (full bath versus half bathrooms), size of the living room, heating mechanism, cooling mechanism, electrical, number of fireplaces, number of fans in the house etc. This data set has many of these attributes included and will be useful in determining the final price.

The data set at hand has a lot of variables that I assume are going to be strongly correlated with the final house price. Initial analysis has revealed that only a few columns has missing data and quality of data is acceptable.

## Author
**Satish Agrawal**

## References
1.	National Association of Realtors  - https://www.nar.realtor/research-and-statistics/housing-statistics/existing-home-sales
2.	Kaggle data set - https://www.kaggle.com/bakar31/eda-house-price-prediction?select=train.csv
3.	Zillow  https://www.zillow.com/homedetails/22803-Hansen-Ave-Elkhorn-NE-68022/91935264_zpid/
4.	Redfin - https://www.redfin.com/NE/Omaha/16823-Pasadena-Ct-68130/home/63901488
5.	Mark Chalon Smith  - https://www.insurance.com/home-and-renters-insurance/home-insurance-basics/5-factors-that-affect-rates.html
6.	Norada - https://www.noradarealestate.com/blog/housing-market-predictions/
7.	James Gheen - https://www.biggerinvesting.com/6-types-of-real-property-infographic-real-estate-investing/
