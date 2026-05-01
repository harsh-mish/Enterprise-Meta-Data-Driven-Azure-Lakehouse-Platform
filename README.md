# Azure Data Engineering Project

<img width="1000" height="500" alt="Architecture" src="https://github.com/user-attachments/assets/3d614eb9-eebf-4594-af8e-8b194477107f" />



# Azure Data Engineering Project

## Overview
This project demonstrates an end-to-end data pipeline built using Azure services. The pipeline automates data ingestion, transformation, storage, and monitoring.

Technologies used:
- Azure Data Factory
- Azure Databricks
- Azure Synapse Analytics
- Azure Logic Apps




## Git Integration in ADF

This project leverages Git integration in Azure Data Factory to enable proper version control and structured development.

Azure Data Factory was connected to a Git repository, where all pipeline components such as pipelines, datasets, and linked services were stored as JSON files. Instead of directly working on the live environment, development was performed in feature branches.

A separate collaboration branch (e.g., main) was used to consolidate changes. After implementing and testing new features in individual branches, changes were merged into the collaboration branch and then published to the Data Factory environment.

This approach ensures:
- Version control of all pipeline changes
- Safe development without impacting production workflows
- Easy rollback to previous versions if needed
- Better collaboration in team environments

Overall, this setup follows industry-standard CI/CD practices, improving reliability, traceability, and maintainability of data pipelines.



<img width="1000" height="500" alt="gir_intigration" src="https://github.com/user-attachments/assets/cb756a84-c95a-44cc-bb11-553ddf0ec81f" />







## Workflow

The project implements a complete end-to-end data pipeline with multiple stages:

### 1. Data Ingestion (Azure Data Factory)
Data is ingested from multiple sources such as SQL databases, CSV files, and REST APIs using Azure Data Factory pipelines.  
ADF handles:
- Copy activities for data movement  
- Incremental data loading  
- Basic validation and error handling  
The ingested data is stored in the raw (landing) zone of Azure Data Lake Storage.

### 2. Data Processing (Azure Databricks)
The raw data is processed and transformed using Azure Databricks notebooks.  
Transformations include:
- Data cleaning (handling nulls, duplicates)  
- Data transformation and formatting  
- Business logic implementation  
- Aggregations and enrichment  
The processed data is then stored in the curated layer of the data lake.

### 3. Data Storage & Analytics (Azure Synapse Analytics)
The transformed data is loaded into Azure Synapse Analytics for analytical processing.  
This includes:
- Loading into dedicated or serverless SQL pools  
- Running SQL queries for analysis  
- Preparing datasets for reporting and BI tools  

### 4. Automation & Orchestration (Azure Logic Apps)
Azure Logic Apps is used to automate workflow execution and monitoring.  
It performs:
- Scheduled or event-based triggers  
- Monitoring pipeline execution status  
- Sending email notifications on success/failure  

### 5. Monitoring & Logging
The entire pipeline is monitored to ensure reliability:
- Pipeline run monitoring in ADF  
- Logging and error tracking  
- Alerting mechanisms for failures  
This ensures quick debugging and operational stability.





<img width="1000" height="500" alt="Workflows" src="https://github.com/user-attachments/assets/d21cc06f-b4c6-49ec-9146-a049a2a943d9" />






## Implementation Screenshots



### Azure Data Factory Pipeline


<img width="1000" height="500" alt="Screenshot 2026-03-22 135338" src="https://github.com/user-attachments/assets/b0179ac0-8dec-4c09-ab7f-0524854ee1a4" />





### Databricks Transformation


<img width="1000" height="500" alt="Screenshot 2026-03-22 201853" src="https://github.com/user-attachments/assets/b8563f21-4a87-4a2d-90b4-2636c6ee2411" />





### Synapse Analytics


<img width="1000" height="500" alt="Screenshot 2026-03-22 134749" src="https://github.com/user-attachments/assets/4942e95b-b0c8-4560-90e5-c673f041a7b5" />





### Logic App Workflow


<img width="1000" height="500" alt="Screenshot 2026-03-22 135526" src="https://github.com/user-attachments/assets/538cc6b8-c0ea-4d5e-b2ef-a113483cc579" />













