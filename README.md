# AWS Big Data Architecture ETL Pipeline Group Project

The group project was to implement an end-to-end ETL pipeline using AWS services to extract insights from London’s household energy consumption dataset (2011-2014) and display results through visualisations.

## Dataset
[Smart Meters in London](https://www.kaggle.com/datasets/jeanmidev/smart-meters-in-london) (Household Electricity Consumption)

## Problem Statements

Target Audience: Consumers and Energy Companies

1. **Are there any households with unusual energy consumption patterns?**
    
    **Objectives:**
    
    - Electricity fraud detection
    - Help consumers avoid paying for energy they did not use
    - Avoid unnecessary worries on faulty electronics

    **Methods (Unsupervised Machine Learning):**

    - K-Means clustering
    - DBSCAN clustering
    - Isolation Forest Anomaly Detection

2. **How can we optimize energy procurement to reduce financial risks associated with demand fluctuations?**
    
    **Objectives:**
    
    - Predict electricity demand based on factors like time period and weather
    - Determine optimal amount of electricity to procure

    **Methods (Supervised Machine Learning):**

    - XGBoost Linear Regressor Model

## Solution (Data Pipeline Architecture)
<img width="850" height="500" alt="Data Pipeline Architecture" src="Data Pipeline Architecture.png">

## Project Contributions
**Preliminary stage**
- Explored services such as DynamoDB (NoSQL database), Lambda and SQS (batch processing)
- Led the team to perform EDA analysis and train XGBoost Linear Regressor Model for Problem Statement 2

**Final Data Pipeline (Problem Statement 2)**
- Created notebook containing EDA and ML model (model training and evaluation) in Sagemaker
    - Ensured that raw data files are present and after triggering the pipeline, new data files are created in AWS S3
- Created Sagemaker ML pipeline so that execution of ML model starts automatically once main data pipeline is triggered
- Debugged code using Cloudwatch logs

