# Azure Data Engineering Project

<img width="500" height="500" alt="Architecture" src="https://github.com/user-attachments/assets/3d614eb9-eebf-4594-af8e-8b194477107f" />



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



<img width="500" height="500" alt="gir_intigration" src="https://github.com/user-attachments/assets/cb756a84-c95a-44cc-bb11-553ddf0ec81f" />




## Workflow

1. Data is ingested from source systems using Azure Data Factory pipelines.
2. The ingested data is processed and transformed using Azure Databricks notebooks.
3. Transformed data is stored in Azure Synapse Analytics for reporting and analysis.
4. Azure Logic Apps is used to trigger alerts/notifications based on pipeline execution status.






