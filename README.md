# Uber Data Analytics Using GCP(Google Cloud Platform)

## Description
In this project, we will analyze Uber data using various tools and technologies, including GCP Storage, Python, Compute Instance, Mage Data Pipeline Tool, BigQuery, and Looker Studio. 

## Architecture Diagram
![Architecture](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/architecture.jpg)

## Technology Used
- Programming Language - Python

Google Cloud Platform
- Google Storage
- Compute Instance
- BigQuery
- Looker Studio
- Modern Data Pipeine Tool - https://www.mage.ai/

## Dataset Used
TLC Trip Record Data Yellow and green taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

Here is the dataset used - [Dataset](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/uber_data.csv)

More info about dataset can be found here:

1. Website - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
2. Data Dictionary - https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Data Model
![Data Model](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/data_model.jpeg)

## Project Execution Flow
- Data will be stored on Google Cloud storage (Raw Data)
- Writing a transformation logic in Python
- Deploy the code to open-source data pipeline tool called MAGE.
- Then, load data into Google Big Query. (Data Warehouse)
- Building final dashboard onto the Looker Studio.
