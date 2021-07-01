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
  teaser: "/assets/SparkAggBackground.png"
  actions:
    - label: "Go to GitHub Repository"
      url: "https://github.com/satishagrawal/DataScience/tree/main/Heart%20Attack%20Prediction"
---

# Train a prediction model to predict the risk of heart attack

**This notebook loads the data set, performs EDA, cleans the data up and trains a few models using exhaustive train techniques to predict if patient risk of heart attack.**

## The Data
The data set has several observations of patients records and the outcome if patient had a heart attack. This data set is pulled from kaggle @ https://www.kaggle.com/kumudadk/heart-attack-prediction-and-analysis?select=heart.csv

## Tasks
1. Load the data and print the schema

3. Join the flight data to airport codes data by matching the IATA code of the originating flight to the IATA code in the airport codes file, then print the schema

4. Remove the following columns from the joined DataFrame:
	-   \_\_index_level_0\_\_
	-   ident
	-   local_code
	-   continent
	-   iso_country
	-   iata_code

5. Rename the following columns:
	-   type: origin_airport_type
	-   name: origin_airport_name
	-   elevation_ft: origin_airport_elevation_ft
	-   iso_region: origin_airport_region
	-   municipality: origin_airport_municipality
	-   gps_code: origin_airport_gps_code
	-   coordinates: origin_airport_coordinates

6. Repeat steps 2-4 for destinations:
	* Join the data on destination airport instead of the origin airport
	* Drop the same columns
	* Rename the same columns using the prefix `destination_airport_` instead of `origin_airport_`
	* Print the schema

7. Create a dataframe using only data from 2008. This dataframe will be a report of the top ten airports by the number of inbound passengers. This dataframe should contain the following fields:
	-   Rank (1-10)
	-   Name
	-   IATA code
	-   Total Inbound Passengers
	-   Total Inbound Flights
	-   Average Daily Passengers
	-   Average Inbound Flights

8. Create a user-defined function in Python that will convert the string coordinates into numeric coordinates

9. Add new columns for:
	*  destination_airport_longitude
	* destination_airport_latitude
	* origin_airport_longitude
	* origin_airport_latitude
		* Then, print the schema

### Rather than providing all of the schema printouts here, they can all be found in the [notebook](https://github.com/SatishAgrawal/SparkAggregations/blob/master/Spark%20Aggregations.ipynb) located in the GitHub repository for this project.

## Author
**Satish Agrawal**
