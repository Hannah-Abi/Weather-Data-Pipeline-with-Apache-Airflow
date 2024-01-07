## Weather Data Pipeline Using Apache Airflow
### Overview 
This project is to build and automate an end to end data platform right from Data Ingestion from [open weather map API](https://openweathermap.org/api), Data Transformation, Data Loading and Reporting.
### Prerequisites
- AWS Cloud Platform
- Apache Airflow
- Visual Studio Code 1.85 (VS Code)
### Complete Project Execution
#### Step 1 - Remotely SSH (connect) VS Code to AWS EC2 (If you already configure to connect, then you can skip this part) 
- The text editor such as VIM and NANO are not easy to use for code developer in the cloud, while VS Cods as a Code Editor is very user friendly and can help transfer and run files easily. The following is the step by step how to configure SSH Visual Studio Code to AWS EC2:
    - When creating an EC2 iunstance, create a keypair 'pem' file that can be used to connect to VS code later on
    - In VS Code:
        1.  Install "Remote-SSH" to VS Code
        2.  Open a remote window >> Connect to host >> Configure SSH host >> Sellect configuration file
        3.  Fill in this code and save. What you need from EC2 Instances to fill in the code:
            - Host: name of the EC2 instance (in this case, Weather-Airflow_Project)
            - Hostname: Public Ipv4 address
            - User: Platform (Ubuntu, for example)
            - IdentifyFile: File path of the pem file downloaded from AWS 
        3.  Open a remote window >> Connect to host >> choose the remote connect I have created " Weather-Airflow_Project" >> Select the platform of the instance (Linux)
#### Step 2 - Edit incound rule 
- The Inbound Rules control the incoming traffic that's allowed to reach the instance.
- The purpose of this is to see the UI of Airflow in the set up port
#### Step 3 - Install dependences and neccessary libraries needed <br>
**`sudo apt update`** - Update the EC2 that have been provisioned <br>
**`sudo apt install python3-pip`** - install Python <br>
**`sudo apt install python3.10-venv`** - Install virtual environment <br>
**`python3 -m venv airflow_venv`** - Create a virtual environment named "airflow_venv"<br>
**`source airflow_venv/bin/activate`** - To actgivate the virtuakl environment
**`sudo pip install pandas`** - install pandas in the provisioned VEN (virtual environment)<br>
**`sudo pip install s3fs`** - To install s3 bucket<br>
**`sudo pip install apache-airflow`** - install Apache Airflow  <br>
**`airflow standalone`** - to call airflow<br> **You will get the username and apassword to access to the current airflow 
#### Step 3 - Creat DAGs
- To open the current airflow environment that has been provision, run this in a new brownser:
  <br>[Public IPv4 DNS](/images/Public IPv4.png).Port (the port to connect the instance)
- In the airflow, create connection to the API
- See the file weather_dag.py



