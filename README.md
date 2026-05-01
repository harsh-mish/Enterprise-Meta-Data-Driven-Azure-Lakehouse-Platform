# Azure Data Engineering Project

<img width="4000" height="2000" alt="Architecture" src="https://github.com/user-attachments/assets/3d614eb9-eebf-4594-af8e-8b194477107f" />




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






