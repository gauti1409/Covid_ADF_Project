**Objective: To develop a project based around reporting and prediction of COVID-19 Spread. To create a data platform from which our data analysts can easily report on the COVID-19 trends using a reporting tool.**


**Solution Architecture:**

1. Ingest the COVID-19 Data from the ECDC website.

2. Use the HTTP Connector within ADF to get the data.

3. For EU Data, keep the population file in an Azure Storage Account and ingest from there. We could get this data directly from Eurostat website but we will instead ingest from an Azure storage account.

4. Both datasets will be ingested in the ADLS Gen2.

5. Use ADF to transform this data. We will use the transformation capability called Data Flows within the Data Factory for the couple of data sets.

6. Use Azure databricks for transformation of one of the datasets. Then, ADF will be used as an orchestration tool rather than a trasnformation tool.

7. All of the transformed data will then be used in our data lake later for use in ML Models by Data Scientists.

8. We will also push the subset of the required data to the SQL database i.e Azure SQL Database so that it can be used for reporting. We will then build a Power BI Report from this data.

   
**Below is the Solution Architecture Diagram referred for this Project**

![image](https://github.com/gauti1409/Covid_ADF_Project/assets/41252711/3fa22bba-f55a-4ed1-8bb0-63256cd0f1f3)



 
