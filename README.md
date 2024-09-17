# Visualizing the currents of change in Maji Ndogo

## Introduction

This Power BI visualization explores..........



**_Disclaimer_**: All datasets and reports do not represent any company, institutions or country but just a fictional dataset to demonstrate capabilities of power BI


## Problem Statement
1. A
2. B
3. C
4. d
5. e
6. f


## Power BI concepts demonstrated
- Modelling
- Filters
- Visualization

## Data Sourcing

Downloaded the csv files from ALX Explore AI Course and extracted it into power bi for cleaning, analysis and visualization.
Data used in this project:

[Md_water_services_data.xlsx](https://github.com/lisaogeya/Visualizing_the_currents_of_change_in_Maji_Ndogo/blob/main/Md_water_services_data.xlsx)

## Data Modelling

- Automatically derived relationships are adjusted to remove and replace unwanted relationships within the model.

Auto model                            |                    Adjusted model
:----------------------------------------:| :----------------------------------------:        
![](auto_model.png)                   |      ![](adjusted_model.png)

- In the locations table. None of the column names (or headers) were imported correctly. So we changed that to enable relationships be established.
  
- In the queue_composition table, removing the first column establishes the relationships.
- In the water_source_related_crimes table, removing the first column to connect the table to the rest of the model.
- Linked water_source_related_crime table to location table using location_id .
- This model is a star schema. There are 6 dimension tables and a fact table, visits.

## Analysis and Visualizations
