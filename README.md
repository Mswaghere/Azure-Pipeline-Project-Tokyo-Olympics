# Azure-Pipeline-Project-Tokyo-Olympics (Azure Data Factory - Databricks - Synapse Analysis)

## Flow Of a Project
![Azure data pipeline olympics](https://github.com/user-attachments/assets/18cc60e7-a77b-49a4-917f-874db55e34e5)

## Step-By-Step Process

### Step 1: Setting Up Azure Resources
Create an Azure Resource Group: Logged in to the Azure portal and created a new resource group to organize project resources.
Setting Up Azure Data Lake Storage Gen2: Created a Data Lake Storage Gen2 account. This will serve as the storage solution for raw and transformed data.
Created Azure Databricks Workspace: Setting up an Azure Databricks workspace for data transformation tasks.
Created Azure Synapse Analytics Workspace: Setting up an Azure Synapse Analytics workspace for data analysis.

### Step 2: Data Ingestion from GitHub Repository
Created an Azure Data Factory Pipeline: Navigated to Azure Data Factory in the Azure portal and created a new pipeline.
Configured the GitHub Connector: Used the HTTP connector in the Data Factory to access the data from the GitHub repository. Setting up the necessary authentication, such as a personal access token, to access the GitHub API.
Define the Data Flow: Used the Copy Data activity to pull the data from the GitHub repository and store it as raw data in Azure Data Lake Storage Gen2.

![Screenshot_20240727_120303](https://github.com/user-attachments/assets/9b41764e-a261-487b-bf8c-6b846ca371ec)



### Step 3: Transform Raw Data Using Databricks
Opened Azure Databricks: Accessed Databricks workspace and created a new notebook.
Loaded Raw Data: Used PySpark to read the raw data stored in Azure Data Lake Storage Gen2.
Transformed the Data: Performed necessary transformations to clean and structure the data. This included filtering, renaming columns, and aggregating data.

![Screenshot_20240727_200004](https://github.com/user-attachments/assets/629ad24b-edd0-4d4e-a77e-52775768ddea)


### Step 4: Analyze Transformed Data Using Azure Synapse Analytics
Opened Azure Synapse Analytics: Navigated to Synapse workspace.
Created a New SQL Pool: Setting up a SQL pool to run SQL queries on transformed data.
Loaded Transformed Data: Used Synapse to connect Azure Data Lake Storage Gen2 and loaded the transformed data for analysis.
Perform Analysis: Wrote SQL queries to analyze the data, generate insights, and create reports based on analysis.

![Screenshot_20240727_120000](https://github.com/user-attachments/assets/8a515139-1985-4ccd-9229-2f1ae34bb0d1)

![Screenshot_20240727_120054](https://github.com/user-attachments/assets/1ee766d8-130c-41a0-85a4-e53c044a7419)

## Summary of Project Flow

1. Data Ingestion: GitHub Repository → Azure Data Factory → Azure Data Lake Storage Gen2 (as raw data)
2. Data Transformation: Azure Data Lake Storage Gen2 (raw data) → Databricks (structured data)
3. Data Analysis: Databricks (structured data) → Azure Synapse Analytics (analysis and reporting)

