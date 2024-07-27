# Home_Sales
## Overview
In this assignment challenge, I utilised SparkSQL to analyse key metrics about home sales data by creating temporary views, caching tables, and partitioning data. The analysis was conducted using Google Collaboratory (Colab) within a Jupyter Notebook file.

## Data Preparation and Initial Analysis
First, I imported the necessary PySpark SQL functions and read the home sales CSV data into a Spark DataFrame. I then created a temporary table named `home_sales` to answer various queries about average home prices based on different criteria, such as the number of bedrooms, bathrooms, and square footage. One specific calculation, the “average price of homes per ‘view’ rating for homes with an average price greater than or equal to $350,000,” was used as a baseline to compare optimised performances using caching and partitioning.

## Performance Optimisation
This process highlights the impact of caching and partitioning on query performance. To optimise performance, I cached the `home_sales` temporary table and compared the runtime of queries using cached data versus non-cached data. Next, I partitioned the data by the `date_built` field and created a temporary table for the parquet data to further test query runtimes. The results showed that the runtimes using the optimised performance methods significantly reduced query runtimes compared to non-optimised queries. 

## Execution Environmnet
The Jupyter Notebook file `Home_Sales.ipynb` is designed for execution in Google Colab and can be run successfully in this environment

## Source of Data
The csv dataset was accessed through a url provided by edX Boot Camps LLC. The url is contained within the notebook. 

## Folder Structure
### Home_Sales (Root Folder)
```
├── Home_Sales.ipynb - Jupyter Notebook containing the anlysis.
```
