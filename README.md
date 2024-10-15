# Migrating Data from On-Premise SQL Server to Azure SQL Server Using Azure Data Factory
This repository provides a step-by-step guide to migrate data from an on-premise SQL Server to Azure SQL Server using Azure Data Factory (ADF) and its Copy Activity. It covers the setup of linked services, datasets, and integration runtime.

![image](https://github.com/user-attachments/assets/c8e609c0-089a-415b-95d9-b51644ca90d9)

# Table of Contents
+ Prerequisites
+ Overview
+ Setup Azure Data Factory
     + Create Integration Runtime
     + Create Linked Services
     + Create Datasets
+ Creating and Running a Pipeline
+ Monitoring the Pipeline
+ Conclusion

## Prerequisites
Before you begin, ensure you have the following:

+ An Azure subscription.
+ Access to Azure Data Factory.
+ An on-premise SQL Server instance.
+ Azure SQL Server and a database to migrate data to.

## Overview
Azure Data Factory is a cloud-based data integration service that allows you to create data-driven workflows for orchestrating and automating data movement and data transformation. This guide will demonstrate how to set up an ADF pipeline that copies data from an on-premise SQL Server to Azure SQL Database.

## Setup Azure Data Factory
### Create Integration Runtime
1. Go to Azure Data Factory: Navigate to your Azure Data Factory instance in the Azure Portal.
2. Manage: Click on the "Manage" tab on the left.
3. Integration Runtimes: Under "Author", select "Integration Runtimes".
4. New: Click on the "+ New" button.
5. Self-hosted: Choose "Self-hosted" to create an integration runtime that can connect to your on-premise SQL Server.
6. Name and Description: Provide a name and description for the integration runtime and click "Create".
7. Download: After creation, download the integration runtime setup file.
8. Install: Install the integration runtime on your on-premise server by running the downloaded file and follow the instructions.

### Create Linked Services
1. Linked Services: Under the "Manage" tab, click on "Linked Services".
2. New Linked Service: Click on "+ New".
3. On-Premise SQL Server:
    + Select "Azure SQL Database".
    + Fill in the required details like server name, database name, and authentication type.
    + Select the integration runtime you created earlier.
    + Test the connection and click "Create".
4. Azure SQL Database:
    + Again, click on "+ New".
    + Select "SQL Server".
    + Provide connection details for your on-premise SQL Server.
    + Test the connection and click "Create".

### Create Datasets
1. Datasets: Go to the "Author" tab, and click on "Datasets".
2. New Dataset: Click on "+ New Dataset".
3. On-Premise SQL Dataset:
    + Choose "Azure SQL Database".
    + Select the linked service created for Azure SQL Database.
    + Specify the table name and schema, then click "OK".
4. Azure SQL Dataset:
    + Choose "SQL Server".
    + Select the linked service created for your on-premise SQL Server.
    + Specify the table name and schema, then click "OK".
  

## Creating and Running a Pipeline
1. Pipelines: Go to the "Author" tab and click on "Pipelines".
2. New Pipeline: Click on "+ New Pipeline".
3. Copy Data Activity:
    + Drag the "Copy Data" activity from the Activities pane to the pipeline canvas.
    + Configure the source and sink datasets (select your on-premise SQL dataset as the source and Azure SQL dataset as the sink).
    + Configure any additional settings as needed.
4. Run Pipeline: Click on "Debug" or "Add Trigger" to run the pipeline.

## Monitoring the Pipeline
1. Monitor: Go to the "Monitor" tab to check the status of your pipeline runs.
2. View Logs: Click on a specific pipeline run to view detailed logs and activity runs.

## Conclusion
You have successfully set up a migration process using Azure Data Factory to copy data from an on-premise SQL Server to Azure SQL Database. You can customize your pipeline further based on your data transformation and movement needs.



  
  
