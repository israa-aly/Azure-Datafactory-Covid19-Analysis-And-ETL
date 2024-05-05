# Overview
This project uses data from the European Centre for Disease Prevention and Control (ECDC) to monitor weekly and daily COVID-19 cases,
deaths,and hospitalizations across Europe using Azure Data Engineering services
# Solution Architecture
![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/f2ccc2af-c620-43e4-8a65-73333339414a)

# Data Ingestion
Data is ingested from Azure Blob Storage and from HTTP connector into Azure Gen2 Data Lake storage account 
in its raw form, which represents the Bronze layer of our architecture.
# 1- Population Data Ingestion 
![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/56537336-d382-42f6-8eb5-8c203932b760)
# 2-ECDC Data Ingestion

![hhPNG](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/74a094a3-975b-4e18-9f87-89d58af33d1e)

# Data Transformation
# 1- Data flow

Cases and deaths data
![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/3f678710-5056-4cc2-b603-c5949e3f1e00)

Hospital admissions data  

![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/9e6e6635-3100-4c3a-a3c8-0af457d01fc6)

# 2-Databricks

The process involves creating a cluster then processing population data using databricks notbook utilizing pyspark.

![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/e26d79c1-8c09-4523-8ca4-73464b4c97c5)

#Data loading

Then loading the processed data into Azure SQL Database which represents our Gold layer that we will use for reporting.

# Workflow Orchesteration
Creating triggers to automate the pipelines Execution daily.

# Visualization using Power BI

![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/2468cfaf-b87a-405f-8e3e-aa1635079a78)


![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/99ad95ad-1c7f-4a08-87a0-1209dd5ab531)


![Capture](https://github.com/israa-aly/Azure-Datafactory-Covid19-Analysis-And-ETL/assets/68852141/9b45c79c-0714-4187-a46a-8a838ff0bd24)


# Resources

European Centre for Disease Prevention and Control (ECDC):https://www.ecdc.europa.eu/en/data-dashboards-and-databases

Project Use Case:https://www.udemy.com/course/learn-azure-data-factory-from-scratch/?kw=azure+data+factory+fo+da&src=sac&couponCode=KEEPLEARNING


