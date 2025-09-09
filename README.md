# Insurance-Data-Dashboard
📊 Insurance Data Report Dashboard

This repository contains an interactive insurance data report dashboard built to analyze insurance claims, policy types, and customer behavior. The dashboard provides valuable insights into claim status, policy distribution, premium amounts, and monthly policy counts.

🚀 Features

Key Metrics Overview

Total Claim Amount

Pending & Settled Claim Amounts

Total Premium Amount

Total Coverage Amount

Total Number of Policies

Visualizations

Count of Policy Types

Policy Status Distribution (Active vs Inactive)

Premium Amount by Policy Type

Claim Amount Analysis by Age Group & Claim Status

Claim Status Distribution (Pending, Settled, Rejected)

Policy Distribution by Gender & Policy Type

Monthly Policy Count Trend

Filters

Policy Type filter for drill-down analysis

Reset button for clearing filters

📁 Repository Structure
📂 Insurance-Dashboard
│-- 📊 Insurance dashboard.png     # Dashboard snapshot
│-- 📑 InsuranceData.csv           # Raw dataset used for visualization
│-- 📜 README.md                   # Documentation
│-- <project files>                # Power BI / Python / Excel files (if added later)

🛠️ Tech Stack

Database: MySQL (data storage)

Data Visualization: Power BI (Dashboard development)

Dataset: CSV file containing insurance claim and policy data

Tools: Excel / Python (optional preprocessing, if included)

📷 Dashboard Preview

📂 Dataset Details

The dataset (InsuranceData.csv) contains the following attributes (sample):

PolicyType – Type of insurance (Health, Auto, Life, Home, Travel)

ClaimStatus – Status of claim (Pending, Settled, Rejected)

ClaimAmount – Amount claimed by customers

PremiumAmount – Policy premium amount

CoverageAmount – Total coverage provided under the policy

Gender – Gender of policyholder

AgeGroup – Old Age, Adult, Young Adult

⚙️ Data Loading Process

Create a MySQL database and table

CREATE DATABASE InsuranceDB;
USE InsuranceDB;

CREATE TABLE InsuranceData (
    PolicyID INT PRIMARY KEY AUTO_INCREMENT,
    PolicyType VARCHAR(50),
    ClaimStatus VARCHAR(50),
    ClaimAmount DECIMAL(15,2),
    PremiumAmount DECIMAL(15,2),
    CoverageAmount DECIMAL(15,2),
    Gender VARCHAR(10),
    AgeGroup VARCHAR(20)
);


Load CSV data into MySQL table

LOAD DATA INFILE '/path/to/InsuranceData.csv'
INTO TABLE InsuranceData
FIELDS TERMINATED BY ',' 
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(PolicyType, ClaimStatus, ClaimAmount, PremiumAmount, CoverageAmount, Gender, AgeGroup);


Connect Power BI to MySQL

Open Power BI Desktop

Go to Home > Get Data > MySQL Database

Enter your MySQL server credentials

Select the InsuranceDB and InsuranceData table

Load the data and build visuals

📈 Insights from Dashboard

Travel policies have the highest claim counts and premiums.

52.65% policies are active while the rest are inactive.

Old Age group has the highest claim amounts compared to Adults and Young Adults.

Rejected claims are higher than pending and settled claims.

Policy sales peaked in September (871 policies).


📌 Future Enhancements

Add interactive Jupyter Notebook for EDA (Exploratory Data Analysis).

Integrate machine learning models for claim settlement prediction.

Automate data pipeline for real-time dashboard updates.

🤝 Contributing

Contributions are welcome! If you’d like to improve this dashboard or extend its functionality, please fork the repo and create a pull request.

📜 License

This project is licensed under the MIT License.
