## Weather Data Pipeline Using Apache Airflow
### Overview 
This project is to build and automate the data pipeline from Data Extraction, Data Transformation, and Data Loading. 
This project is to create an end to end data platform right from Data Ingestion from [open weather map API](https://openweathermap.org/api), Data Transformation, Data Loading and Reporting. The use case for this project is building an end to end solution by ingesting the tables from HTTP serverusing Azure Data Factory and then store the data in Azure Data Lake Gen2. Then Azure databricks is used to transform the RAW data to the most cleanest form of data and then I use Azure Synapse Analytics to load the clean data and finally using Microsoft Power BI to integrate with Azure synapse analytics to build an interactive dashboard.
### Prerequisites
- AWS Cloud Platform
- Apache Airflow
- Visual Studio Code 1.85 (VS Code)
### Complete Project Execution
Step 1 - Remotely SSH (connect) VS Code to AWS EC2 (If you already configure to connect, then you can skip this part) 
- The text editor such as VIM and NANO are not easy to use for code developer in the cloud, while VS Cods as a Code Editor is very user friendly and can help transfer and run files easily. The following is the step by step how to configure SSH Visual Studio Code to AWS EC2:
    - In VS Code:
        1.  Install "Remote-SSH" to VS Code
        2.  Open a remote window >> Connect to host >> Configure SSH host >> Sellect configuration file
        3.  Fill in this code and run. What you need from EC2 Instances to fill in the code:
            - Host: name of the EC2 instance
            - Hostname: Public Ipv4 address
            - User: Platform (Ubuntu, for example)
            - IdentifyFile 


