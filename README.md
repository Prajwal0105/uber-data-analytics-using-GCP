# Uber Data Analytics Using Google Cloud Platform (GCP)

## Project Overview
This project aims to analyze Uber trip data using various tools and technologies offered by **Google Cloud Platform (GCP)**. The end-to-end data pipeline integrates raw data ingestion, transformation, storage, and visualization, offering valuable insights into Uber trips. The core technologies involved include **Python**, **GCP Storage**, **Mage Data Pipeline Tool**, **BigQuery**, and **Looker Studio** for building an interactive dashboard.

By the end of this project, you'll gain insights into trip details such as pick-up and drop-off times, trip distances, fare breakdowns, and more, through an organized data pipeline and visualizations.

---

## Architecture Overview
Below is the architecture diagram of the Uber Data Analytics pipeline:

![Architecture](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/architecture.jpg)

The architecture follows a structured approach to ensure scalability, reliability, and efficiency throughout the pipeline.

1. **Data Ingestion**: Raw trip data is collected and stored in **Google Cloud Storage**.
2. **Transformation**: Python scripts are used to clean, preprocess, and transform the raw data into a more usable format.
3. **Pipeline Orchestration**: Transformation logic is deployed using **Mage.ai**, a modern data pipeline tool.
4. **Data Loading**: The cleaned data is loaded into **Google BigQuery**, which serves as the data warehouse.
5. **Data Visualization**: **Looker Studio** is used to create visual dashboards for analyzing key metrics.

---

## Technologies and Tools Used

### Programming Language:
- **Python**: For writing scripts to clean and transform raw data, and handling business logic for data pipelines.

### Google Cloud Platform Services:
- **Google Cloud Storage**: Used for storing raw Uber trip data, which includes details like pick-up/drop-off times, trip distances, and fares.
- **Google Compute Instances**: Provides compute power to execute the Python scripts responsible for transforming the data.
- **Google BigQuery**: A scalable data warehouse where cleaned and structured data is stored for analysis.
- **Looker Studio**: A visualization tool that enables you to build dynamic dashboards and share them with stakeholders.

### Additional Tools:
- **Mage.ai**:  
  Mage is an open-source tool used for orchestrating data pipelines. In this project, Mage is used to deploy transformation scripts, manage workflows, and move data between storage, transformation, and warehouse stages.  
  [Learn more about Mage](https://www.mage.ai/)

---

## Dataset Information
This project leverages the **TLC Trip Record Data**, which includes detailed records of Uber, yellow, and green taxi trips in New York City. The dataset captures a variety of fields that are essential for analysis, such as:

- **Pick-up and Drop-off Times**: The precise timestamps when a trip starts and ends.
- **Pick-up and Drop-off Locations**: Geo-coordinates of where the trip begins and ends.
- **Trip Distance**: The distance traveled during the trip, measured in miles or kilometers.
- **Fare Breakdown**: Itemized details of the trip fare, including base fare, taxes, surcharges, and tolls.
- **Rate Types**: Whether the fare is flat-rate or metered.
- **Payment Types**: Methods of payment used by passengers (e.g., cash, credit card).
- **Passenger Count**: Number of passengers on each trip as reported by the driver.

The dataset used in the project can be accessed here:  
**[Download Dataset](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/uber_data.csv)**

For more details about the dataset, visit:
- **Website**: [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
- **Data Dictionary**: [TLC Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf)

---

## Data Model
The data model for this project is designed to optimize analysis and querying in **Google BigQuery**. It is structured to efficiently handle large volumes of Uber trip data and provide seamless querying for various metrics such as trip distances, fare totals, and trip duration.

Below is the data model that represents how the data is organized after transformation:

![Data Model](https://github.com/Prajwal0105/uber-data-analytics-using-GCP/blob/main/data_model.jpeg)

---

## Project Execution Flow
The project follows a structured approach from data ingestion to visualization. Here's a step-by-step breakdown of the execution process:

### 1. **Data Ingestion**
Raw trip data, collected from the **TLC Trip Record Data**, is stored in **Google Cloud Storage**. This raw data consists of numerous fields, such as timestamps, locations, fare details, and other trip-related information.

- **Google Cloud Storage** acts as the staging area for the unprocessed trip data.

### 2. **Data Transformation**
Next, transformation logic is implemented using **Python**. This involves cleaning and structuring the raw data for further analysis. Some of the key transformation steps include:
- Handling missing values.
- Standardizing time formats.
- Aggregating fare components.
- Geospatial transformations to handle latitude and longitude fields.

This transformation logic is deployed using **Mage.ai** to orchestrate the pipeline.

### 3. **Pipeline Orchestration**
Once the transformation logic is defined, it is integrated into the **Mage Data Pipeline Tool**. Mage allows the automation and scheduling of ETL jobs, ensuring the data is transformed and ready for analysis in BigQuery.

- **Mage.ai** facilitates a modern, scalable approach to ETL.

### 4. **Data Loading into BigQuery**
After transformation, the clean data is loaded into **Google BigQuery**, where it is stored as structured tables for analysis. BigQuery allows for fast querying of large datasets, making it the ideal platform for storing and querying Uber trip data.

- **BigQuery** serves as the data warehouse where all final, cleaned data is stored.

### 5. **Data Visualization Using Looker Studio**
The final step involves building dynamic dashboards in **Looker Studio**. These dashboards allow stakeholders to explore key metrics such as:
- Total trip count.
- Average trip distance.
- Total revenue generated.
- Distribution of payment methods.

**Looker Studio** offers interactive visualizations that help stakeholders make data-driven decisions based on real-time insights from the Uber trip data.

---

## Conclusion
This project demonstrates how to effectively leverage Google Cloud Platform services, Python, and modern data pipeline tools like Mage.ai to analyze Uber trip data. From ingestion and transformation to analysis and visualization, the pipeline provides a comprehensive, scalable solution for deriving insights from large datasets.
