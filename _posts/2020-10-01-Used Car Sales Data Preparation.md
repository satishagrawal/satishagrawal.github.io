---
title: "Data cleaning and preparation for used car sales data"
date: 2020-09-30
tags:
 - Python
 - Jupyter Notebook
excerpt: "Demonstrate the steps in data cleaning and data preparation using used car sales dataset"
header:
  overlay_image: "/assets/datacleaning.jpg"
  overlay_filter: 0.3 # same as adding an opacity of 0.3 to a black background
  teaser: "/assets/datacleaning.jpg"
  actions:
    - label: "Go to GitHub Repository"
      url: "https://github.com/satishagrawal/DataScience/tree/main/Used%20Car%20Sales%20Data%20Preparation"
---

# Data cleaning and preparation
**This study combines NHL player statistics, player contract information, and economic data to predict a player’s value- locally adjusted for a specific team**

## Introduction
For this project I chose used cars datasets from variety of sources including a flat file like CSV, a webpage in tabular format and an API which can be accessed via restful GET endpoints. Below are the three data sources with description of data in there:

1.	A CSV file: This CSV file is downloaded from Kaggle [1]. It contains Car’s data, scraped from AUCTION EXPORT.com. This dataset included Information about 28 brands of clean and used vehicles for sale in US. There are twelve features assembled for each car in this dataset. This data set includes basic car attributes like brand, model, year, color, the sale price for the car, vin (vehicle identification number) and mileage. It also includes other information like, state and city of the car location, title status, the lot number and condition.

2.	A web page: The second source of cars data is from true car website where it has all the cars listed for sale [2]. This web site provides a variety of filters to pinpoint to small number of listed cars to limit the result set. This site provides multiple car attributes like interior color, exterior color, make model, year, mileage and many other attributes that define the car and its condition.

3.	An API: The third source of data is a marketplace for API which provides information related to cars [3]. This API gateway site has many different APIs that provide data like inventory of cars, VIN history, Dealer info API, and other market statistics related data APIs. For this project I am concentrating on the statistics API which provides popular cars by city state pair. I have subscribed to the API for a trial to review the data and see any possible connections with other two data sources. This API provides the max and min price of the popular cars, with mean, variance and standard deviation. It also mileage statistics like min, max, median and variance. Other basic info like make and model are also provided.

### Refer to the notebook for data cleaning and preparation steps

## Author
**Satish Agrawal**

## References:
[1] https://www.kaggle.com/doaaalsenani/usa-cers-dataset
[2] https://www.truecar.com/used-cars-for-sale/listings/
[3] https://apidocs.marketcheck.com/?version=latest#5be79d1e-2756-4cae-845f-8dc28fbf8a3c
