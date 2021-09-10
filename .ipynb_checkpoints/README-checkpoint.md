![img](./img/cover.jpg)

# Pump it Up: Data Mining the Water Table


## Overview

Using data from Taarifa and the Tanzanian Ministry of Water, can you predict which pumps are functional, which need some repairs, and which don't work at all? This is an intermediate-level practice competition. Predict one of these three classes based on a number of variables about what kind of pump is operating, when it was installed, and how it is managed. A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

 
## Business Problem

Over 24 million people are impacted by the The United Republic of Tanzania’s water crisis; that’s almost half of the population of Tanzania

A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

The goal is to predict the operating condition of a waterpoint for each record in the dataset.

![img](./viz/pumps_scatter.png)

## Data

The Water Table dataset contains almost 60.000 records of water pumps information across Tanzania. The following set of information about the waterpoints were provided:

- amount_tsh - Total static head (amount water available to waterpoint)
- date_recorded - The date the row was entered
- funder - Who funded the well
- gps_height - Altitude of the well
- installer - Organization that installed the well
- longitude - GPS coordinate
- latitude - GPS coordinate
- wpt_name - Name of the waterpoint if there is one
- num_private -
- basin - Geographic water basin
- subvillage - Geographic location
- region - Geographic location
- region_code - Geographic location (coded)
- district_code - Geographic location (coded)
- lga - Geographic location
- ward - Geographic location
- population - Population around the well
- public_meeting - True/False
- recorded_by - Group entering this row of data
- scheme_management - Who operates the waterpoint
- scheme_name - Who operates the waterpoint
- permit - If the waterpoint is permitted
- construction_year - Year the waterpoint was constructed
- extraction_type - The kind of extraction the waterpoint uses
- extraction_type_group - The kind of extraction the waterpoint uses
- extraction_type_class - The kind of extraction the waterpoint uses
- management - How the waterpoint is managed
- management_group - How the waterpoint is managed
- payment - What the water costs
- payment_type - What the water costs
- water_quality - The quality of the water
- quality_group - The quality of the water
- quantity - The quantity of water
- quantity_group - The quantity of water
- source - The source of the water
- source_type - The source of the water
- source_class - The source of the water
- waterpoint_type - The kind of waterpoint
- waterpoint_type_group - The kind of waterpoint

The labels in this dataset are simple. There are three possible values:

- functional - the waterpoint is operational and there are no repairs needed
- functional needs repair - the waterpoint is operational, but needs repairs
- non functional - the waterpoint is not operational

## Methods




## Results

Key factors that has the most significant impact on the classification results:
- Square footage - a 10% increase in the house square footage leads to a 8% increase in price
- Waterfront properties - the price of the house increases by 107% if waterfront equals 1
- Distance from Seattle/Bellevue - a 10% increase in distance from the epicenter leads to a 3% decrease in price
- Basement - the price of the house increases by 32% if the house has a basement (equals 1)
- Zip code - the price of the house increases by 22% when increasing the zip code category by 1

![img](./viz/feature_imp.png)


## Conclusions

This analysis leads to three conclusions regarding the price and the most significant factors that have an impact on the price:

- **Waterfront properties can increase the price over 100%** Properties that face the waterfront are significantly more expensive than other similiar properties. 
- **Price of property is affected by the mean property price in a given zipcode.** The neighbourhood and price levels in each zipcode has an impact on the price. 
- **Location, location, location** The closer the property is located to Seatlle and Bellevue the more expensive it gets. Every 10% increase in the distance from the epicenter leads to a 3% decrease in price

### Next Steps

Using the prediction model can help to eastimate the property price and and find properties with a price increase potential when searching for a house. The model also helps to estimate the best list and sale price range:

- **Good tool to find an investment property** If you're looking for a property below the market price, this tool can help to find, check and compare the house price with the estimated market price.
- **Find out what's the best list and sale price** It's always the biggest question mark what price I should list and sell my house for. Use the model to find the right one and know the wiggle room. 


## For More Information

See the full analysis in the [Jupyter Notebook](./LR Model - Test 9.ipynb) or review this [presentation](./KING COUNTY HOUSE SALES - LINEAR REGRESSION MODEL.pdf).

## Repository Structure

```
├── img
├── README.md
├── kc_house_data.csv
├── df_processed.pickle
├── LR Model - Test 9.ipynb
└── KING COUNTY HOUSE SALES - LINEAR REGRESSION MODEL.pdf
```
