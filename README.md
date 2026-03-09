# GDP Prediction using Machine Learning and Business Intelligence

## Overview

This project develops a data-driven framework for analyzing and predicting Gross Domestic Product (GDP) using macroeconomic indicators. The system integrates real-world economic data from the World Bank with Business Intelligence dashboards and machine learning models to explore economic patterns and generate predictive insights.

The project combines data visualization and predictive analytics to provide a comprehensive view of global economic performance.

---

## Objectives

- Analyze GDP trends using Business Intelligence dashboards.
- Explore relationships between GDP and macroeconomic indicators.
- Develop machine learning models to predict GDP values.
- Provide interactive dashboards for economic data exploration.
- Demonstrate the use of data analytics in economic forecasting.

---

## Dataset

The dataset used in this project is obtained from:

**World Bank Open Data**  
https://data.worldbank.org/

### Key Variables

- GDP
- Population
- Inflation
- Imports
- Exports
- Country
- Year

These variables were selected to study the relationship between economic indicators and GDP growth.

---

## System Architecture

The system follows a data analytics pipeline:

1. Data Collection  
2. Data Cleaning and Preprocessing  
3. Data Modeling (Star Schema)  
4. Business Intelligence Dashboard Development  
5. Machine Learning Model Training  
6. GDP Prediction and Analysis  

---

## Data Model

A **Star Schema** was implemented to organize the dataset for efficient analysis.

### Fact Table

**Fact_GDP**

- GDP  
- Population  
- Inflation  
- Imports  
- Exports  

### Dimension Tables

- Dim_Country  
- Dim_Time  

This structure enables multidimensional analysis across countries and time periods.

---

## Dashboards

The Power BI report contains four interactive dashboards:

### 1. GDP Overview
Provides a high-level summary of global GDP trends across different years.

### 2. Macroeconomic Indicators
Analyzes relationships between GDP and macroeconomic variables such as population and inflation.

### 3. Model Results
Displays the performance of machine learning models used for GDP prediction.

### 4. Country Deep Dive
Allows detailed analysis of GDP and economic indicators for individual countries.

---

## Machine Learning Models

The project uses regression-based machine learning models for GDP prediction.

### Models Implemented

- Decision Tree Regression
- Random Forest Regression

These models were trained using macroeconomic indicators to estimate GDP values.

---

## Model Evaluation Metrics

The models were evaluated using standard regression metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Random Forest Regression produced more stable and accurate predictions.

---

## Tools and Technologies

- Python
- Pandas
- Scikit-learn
- Power BI
- Jupyter Notebook
- World Bank Open Data

---

## Key Insights

- Global GDP shows a long-term upward growth trend.
- Macroeconomic indicators influence GDP performance.
- Population and trade activity show strong relationships with economic growth.
- Machine learning models can effectively predict GDP trends.

---

## Future Scope

- Integrate additional economic indicators such as unemployment and investment data.
- Apply advanced regression techniques like Gradient Boosting or XGBoost.
- Extend the dataset using longer historical economic data.
- Develop automated forecasting pipelines for continuous economic monitoring.

---

