# Azure-Based ETL Pipeline for OTT Platform Data

## Project Overview
Developed an ETL pipeline for OTT platform data, focusing on data from popular platforms like Netflix, Disney+, and Prime.

## Tools & Platforms Used
- Azure
- Azure Datalake Storage Gen2
- Azure Data Factory
- Azure Synapse Analytics
- Azure SQL Database
- Azure Logic App
- PowerBI
- Azure DevOps Git
- Microsoft SSMS
- Email Notifications

## Data Extraction
- Utilized a dummy dataset of OTT platforms from Kaggle.
- Configured a budget in Azure for email alerts when crossing set expense thresholds.
- Set up Azure infrastructure, including a resource group, Azure Datalake Storage Gen2, Azure Data Factory, Azure Synapse Analytics, and Azure SQL Database.

## Azure Data Factory Ingestion
- Employed a self-hosted runtime for data transition from on-premise to Azure Data Lake Gen2.
- Integrated Azure Key Vault for enhanced data security and used linked services for smooth data transfer between on-premise and cloud.
- Created pipelines to channel data into a 'raw' folder in Azure Data Lake Gen2.
- Incorporated two strategies for incremental data loading:
  - Based on the 'last modified' timestamp of files.
  - Using date details from filenames like "2022-04-12 110513.455313" for day-specific data ingestion.

## Efficiency Enhancements in Data Lake
- Implemented a method to distribute incoming data into folders designated by date, rather than a single large 'raw' folder.
- Utilized this data structure in Azure Synapse to only transform the current day's data.

## Transformation
- Set up a link between Azure Datalake and Synapse Notebook, initiating a spark pool with three worker nodes for optimized code execution.
- Undertook data cleaning tasks: managing NULL values, eliminating duplicates, modifying column types, and engineering features.
- Stored the refined data back in Datalake and relayed it to the SQL database. 

## Automation & Orchestration
- Orchestrated pipelines for extraction, loading, and transformation.
- Established daily triggers for execution at 12 pm.
- Incorporated Azure Logic App for email notifications during any stage of pipeline failures.

## Visualization with PowerBI
- Curated a PowerBI dashboard featuring five insightful charts. [Explore the dashboard here](https://lnkd.in/evR8V4Cm).

## CI/CD Integration
- Set up a CI/CD pipeline in Azure DevOps Git for the mentioned pipeline.
- Collaborated with Zaid Chaudhary on the DevOps Git project.
- Zaid initiated a new branch in the DevOps Git project, architected a new pipeline, and forwarded pull requests for review.
- Changes approved and integrated into the main project branch.



