![img](./img/cover.jpg)

# Pump it Up: Data Mining the Water Table


## Overview

Using data from Taarifa and the Tanzanian Ministry of Water, can you predict which pumps are functional, which need some repairs, and which don't work at all? This is an intermediate-level practice competition. Predict one of these three classes based on a number of variables about what kind of pump is operating, when it was installed, and how it is managed. A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

 
## Business Problem

Over 24 million people are impacted by the The United Republic of Tanzania’s water crisis; that’s almost half of the population of Tanzania

A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

The goal is to predict the operating condition of a waterpoint for each record in the dataset.

![img](./img/pumps_scatter.png)

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

![img](./img/labels_dist.png)

## Methods

Machine learning - Multiclass classification with XGBoost


## Results

Key variables that have the most significant impact on the classification results:

![img](./img/feature_imp.png)


## Conclusions

The model accurancy was approximately 71%. 


## For More Information

See the full analysis in the [Jupyter Notebook](./Model_training.ipynb) or review this [presentation](./Pump It Up Presentation.pdf).

## Repository Structure

```
├── img
├── README.md
├── Water_Table_Submission_format.csv
├── Water_Table_Test_set_values.csv
├── Water_Table_Training_set_labels.csv
├── Water_Table_Training_set_values.csv
├── X_processed.pickle
├── Submission.ipynb
├── Model_training.ipynb
├── EDA.ipynb
└── Pump It Up Presentation.pdf
```
