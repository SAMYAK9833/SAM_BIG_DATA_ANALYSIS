
# Big Data Analysis on NYC Taxi Trips Using PySpark 

## Project Overview :-

This project performs large-scale analysis on the NYC Yellow Taxi Trip dataset using PySpark, a powerful big data processing framework. The goal is to demonstrate the scalability and performance of PySpark in handling millions of records while uncovering insights into taxi trip patterns, such as fare amounts, passenger counts, and trip distances. The project includes data loading, cleaning, and exploratory data analysis (EDA) to derive actionable insights from the dataset.

## Features :-

- Data Loading :- Reads large CSV files using PySpark for efficient processing.

- Data Cleaning :- Filters out invalid records (e.g., negative fares, zero distances, or zero passengers).

- Exploratory Data Analysis :- 
1. Identifies the top 5 most common passenger counts.
2. Calculates average fares by trip distance buckets (<2 km, 2-5 km, >5 km).

3. Lists the top 5 most expensive trips based on total amount.

- Scalability: Leverages PySpark's distributed computing to handle large datasets.

## Prerequisites :-

### To run this project, you need the following tools and libraries :- 

- Python (version 3.6 or higher)

- PySpark (version 3.x)

- Google Colab (optional, for cloud-based execution)

- Google Drive (optional, for mounting datasets in Colab)
- NYC Yellow Taxi Trip Data 

## Installation :-

### 1. Install PySpark :-
```
pip install pyspark
```
### 2. Download the Dataset :-

- Obtain the NYC Yellow Taxi Trip dataset (e.g., yellow_tripdata_2015-01.csv) from the NYC Taxi & Limousine Commission or another reliable source.

- Place the dataset in a directory accessible to your script (e.g., /content/drive/MyDrive/Big Data/ if using Google Colab).

### 3. Set Up Google Colab (Optional) :-
#### If using Google Colab, mount your Google Drive to access the dataset :-
~~~
from google.colab import drive
drive.mount('/content/drive')
~~~

## Key Analyses :-
- Passenger Count Distribution :- View the top 5 most common passenger counts.

- Average Fare by Distance Bucket :- Analyze fares for trips grouped by distance (<2 km, 2-5 km, >5 km).

- Most Expensive Trips :- Identify the top 5 trips with the highest total amounts.

## Example Output :- 
- Top 5 Passenger Counts :-
~~~
+---------------+-------+
|passenger_count|  count|
+---------------+-------+
|              1|8926120|
|              2|1805631|
|              5| 695437|
|              3| 526031|
|              6| 453123|
+---------------+-------+
~~~
- Average Fare by Distance Bucket :-
~~~
+---------------+------------------+
|distance_bucket|          avg_fare|
+---------------+------------------+
|         2-5 km|13.088639505102561|
|          <2 KM|  6.93148657784056|
|         > 5 KM| 31.27973626017181|
+---------------+------------------+
~~~
- Top 5 Most Expensive Trips :-
```
+-------------+-----------+-------+----------+------------+---------------------+------------+
|trip_distance|fare_amount|mta_tax|tip_amount|tolls_amount|improvement_surcharge|total_amount|
+-------------+-----------+-------+----------+------------+---------------------+------------+
|         5.32|       22.0|    0.5| 3950588.8|         0.0|                  0.3|   3950611.6|
|          1.7|     4008.0|    0.5|       0.0|         0.0|                  0.3|      4009.3|
|          0.4|     3005.5|    0.5|       0.0|         0.0|                  0.3|     3006.35|
|         18.5|       52.0|    0.5|       0.0|     1450.09|                  0.3|     1502.89|
|         10.8|       32.5|    0.5|       0.0|     1000.66|                  0.3|     1034.46|
+-------------+-----------+-------+----------+------------+---------------------+------------+
```
## Screenshot :-

<img width="1364" height="768" alt="Image" src="https://github.com/user-attachments/assets/b9683a62-130a-4d38-8387-5f90f731ae51" />


## Author

**SAMYAK VAIDYA**  
Artificial Intelligence & Data Science Enthusiast  
Connect on [LinkedIn](https://www.linkedin.com/in/samyak-vaidya-4bb9b4282)
