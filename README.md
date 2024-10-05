# Visualizing the currents of change in Maji Ndogo

## Introduction

This project, a continuation of [Maji Ndogo's past](https://github.com/lisaogeya/Gender-Inequality-IN-Water-Access) , aims to provide a comprehensive analysis of water access and source utilization in the regions of Maji Ndogo. By visualizing queue compositions of men, women, and children over different days and across various provinces, we can understand how different demographics are accessing these vital resources. Using Power BI, we explore water usage patterns, highlighting the gender distribution in queues at multiple water sources, including wells, rivers, and shared taps. This approach offers insights into potential disparities in access and allows us to identify days with longer queues and higher demand.

Beyond queue analysis, the project delves into environmental factors, specifically water source pollution across the provinces. By tracking pollution levels, we can identify sources that require immediate attention and repair.Through these visualizations, stakeholders can make informed decisions and allocate the necessary budget for maintaining and improving water access infrastructure.



**_Disclaimer_**: All datasets and reports do not represent any company, institutions or country but just a fictional dataset to demonstrate capabilities of power BI


## Problem Statement
1. Which days of the week have consistently longer queues compared to weekends?
2. What is the percentage of children in both long and short queue days, and how is this related to the presence of women in the queue?
3. What is the average composition of queues on various days?
4. What are the average queue times per hour of the day?
5. Which day of the week has the highest queue times overall?
   


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
- In this model:
   - There are 4 dimension tables to the visits fact table.
   - Project_progress and water_source_related_crimes are fact tables on their on.
- Thus the model is a multi-star schema.

## Data Transformation
- In the locations table. None of the column names (or headers) were imported correctly. So that was changed  to enable relationships be established.
- In the queue_composition table, removing the first column establishes the relationships.
- In the water_source_related_crimes table, first column was removed to connect the table to the rest of the model.
- Linked water_source_related_crime table to location table using loc_id and location_id respectively.


## Analysis and Visualizations
**National Overview of distribution of water sources**
![](national_distr_pg.png)
**Insights**
- Shared taps is the most popular popular water source serving 43% of the population in Maji Ndogo, rivers being the least popular catering to 8% of the population.
  

**Average Queue times**
![](average_queues.png)
**Insights**
- In Amanzi the average queue is mostly made up of men although on the national level it is mostly women.
- On Saturdays, queues across Maji Ndogo are 40% men and on Mondays, 71% women.
- Saturday has the highest queue times overall while Sunday has the lowest queue times.
- On weekdays Monday has the longest queues while Wednesday has the shortest queues.
