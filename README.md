# Retail Sales Analysis

**Technical Exam for Job Application: Analyzing Retail Sales Data**

## Project Description

This project focuses on analyzing and predicting customer behavior using retail sales data. The goal is to conduct exploratory data analysis (EDA), clean the dataset, perform a cohort analysis, develop predictive models to estimate the likelihood of repeat purchases, and create visualizations to support the findings.

The analysis identified Random Forest as the most effective predictive model for estimating the likelihood of repeat purchases. It was selected based on its superior performance across key metrics, including accuracy, F1 score, recall, and precision. This model provides valuable insights into customer behavior, allowing for more accurate predictions of future purchases.

## Dataset

The dataset used in this project is from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail). It includes transactional data from a retail company that sells a wide range of unique products. The dataset contains various columns, including `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, and `Country`. 

### Key Features:
- **InvoiceNo**: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction.
- **StockCode**: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product name. Nominal.
- **Quantity**: The quantities of each product per transaction. Numeric.
- **InvoiceDate**: Invoice date and time. Numeric, the day and time when a transaction was generated.
- **UnitPrice**: Unit price. Numeric, Product price per unit.
- **CustomerID**: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- **Country**: Country name. Nominal, the name of the country where a customer resides.

**To install the dataset use (as made in the data_preparation.ipynb:**

```python
   pip install ucimlrepo
   
   from ucimlrepo import fetch_ucirepo 
  
   # fetch dataset 
   online_retail = fetch_ucirepo(id=352) 
   ```

## Phases of the Project

### 1. **Data Preparation and Cleaning**
   - **Objective**: Clean the dataset to ensure accuracy, completeness, and consistency.
   - **Process**:
     - **Missing Values**: Identified and handled missing values in crucial columns like `CustomerID` and `Description`.
     - **Data Quality**: Corrected data quality issues, including removing duplicates and handling missing values.
     - **Exploratory Data Analysis (EDA)**: Generated visualizations and summary statistics to understand the data distribution.
   - **Notebook**: `data_preparation.ipynb`
     - Contains code for the data cleaning process, with explanations and visualizations.
   
### 2. **Cohort Analysis**
   - **Objective**: Understand customer retention and behavior over time.
   - **Process**:
     - **Cohort Labels**: Created cohort labels based on the first purchase date of customers.
     - **Cohort Analysis**: Analyzed the behavior of different customer cohorts over time, focusing on retention rates.
     - **Visualizations**: Cohort tables and heatmaps were generated to illustrate the findings.
   - **Notebook**: `cohort_analysis.ipynb`
     - Contains the cohort analysis process, with step-by-step code and visualizations.
   
### 3. **Predictive Modeling**
   - **Objective**: Develop models to predict the likelihood of customers making a purchase in the next 30 days.
   - **Process**:
     - **Feature Engineering**: Created features like Recency, Frequency, and Monetary (RFM) scores to quantify customer behavior.
     - **Model Selection**: Evaluated different models (e.g., Random Forest, XGBoost) based on accuracy, precision, recall, and F1-score.
     - **Prediction**: Generated probabilities for whether a customer would purchase in the next 30 days.
   - **Notebook**: `predictive_models.ipynb`
     - Details the model development process, including training, evaluation, and predictions.

## Installation

To set up the environment, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Retail-sales-analysis.git
   cd Retail-sales-analysis
   ```

2. **Install Requirements**:
   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` includes all necessary Python libraries, such as pandas, numpy, scikit-learn, xgboost, plotly, etc.


