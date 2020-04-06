# About this Project
Perform simple prediction of world population using linear regression using different data science tools

# Target
Learn complete data science workflow and how to integrate different data science tools in the workflow 

# Data
Data includes the population of 264 countries 
* [from 1960 to 1990](https://github.com/khuyentran1401/world-population-prediction/blob/master/world-population-prediction/1960-Worksheet%20in%20World%20Population%20Prediction%20Model5.csv)
* [from 1991 to 2018](https://github.com/khuyentran1401/world-population-prediction/blob/master/world-population-prediction/Worksheet%20in%20World%20Population%20Prediction%20Model6.csv)

# Tools
* **Amazon Relational Database Service (Amazon RDS)**: tool to set up, operate, and scale MySQL deployments in the cloud
* **Amazon Elastic Compute Cloud (Amazon EC2)**: tool to provide secure, resizable compute capacity in the cloud
* **MySQL**: tool to create table and store database
* **Talend ETL**: tool to load data into MySQL
* **Tableau**: tool to visualize data 

# Project Workflow
![workflow](https://github.com/khuyentran1401/world-population-prediction/blob/master/images/Screenshot%202020-04-05%2019.20.49.png)

# Steps
* Setup: 
  * Launching a MySQL database instance in my AWS account
  * Launching an EC2 instance
  * Connect to EC2 instance via SSH
  * Connect to the databsase in AWS from my computer (via EC2) to interact with it using SQL
  * Conect Talend ETL to AWS RDS
  * Upload data to Talend ETL then transfer the data to AWS RDS
  * Connect MySQL to Python with PyMySQL
  * Integrate 2 data and create prediction file in Python
  * Load the data on Talend ETL then transfer the data to AWS RDS
  * Connect Tableau to AWS RDS and visualize
  
  _Find more instructions about the setup [here](https://github.com/khuyentran1401/world-population-prediction/blob/master/pdf/AWS%20and%20MySQL%20Connection%20Instruction%20-%20Arch%20Talents.pdf)_ and [here](https://docs.google.com/presentation/d/1ompgqRMrVLoMSsqvq_amTdVTw6mfsB4pZcsyi-UMiSY/edit?usp=sharing)_
  

* Preprocessing and Model Training in Python
_The notebook can be found [here](https://github.com/khuyentran1401/world-population-prediction/blob/master/world-population-prediction/Word%20Prediction.ipynb)
  * Preprocessing:
    * Fill in missing values with fill forward method
  * Visualization:
    * Use Plotly and `interact` method of ipywidgets to visualize the data
    ![population](https://github.com/khuyentran1401/world-population-prediction/blob/master/images/population.gif)
  * Prediction:
    * Since the population trends of many countries are linear and for the simple purpose of practicing with the tools, I with linear regression to predict the population from 2019 to 2021
    * Score: 0.994
    * Find the prediction csv file [here](https://github.com/khuyentran1401/world-population-prediction/blob/master/world-population-prediction/Word_Prediction2021.csv)
