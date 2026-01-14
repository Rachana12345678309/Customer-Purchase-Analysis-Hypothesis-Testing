# Customer Purchase Analysis & Hypothesis Testing

An end-to-end data analysis project focused on understanding consumer purchase behavior through Exploratory Data Analysis (EDA) and rigorous statistical hypothesis testing using Python.

## Overview

This project analyzes a large-scale retail dataset (purchase records) to extract meaningful insights about customer demographics and spending habits. Beyond descriptive analysis, the project implements several inferential statistical tests to validate observations regarding average spending across different gender and age groups.

## Dataset

- **Source:** Retail purchase dataset (`purchase_data.csv`), originally shared via Google Drive.
- **Rows:** 263,015 records.
- **Key columns:**
  - `User_ID`: Unique identifier for each customer.
  - `Gender`: M/F classification.
  - `Age`: Categorical age groups (e.g., 0-17, 18-25, etc.).
  - `Occupation`: Occupation code of the customer.
  - `City_Category`: Category of the city (A, B, or C).
  - `Stay_In_Current_City_Years`: Duration of residency in the current city.
  - `Marital_Status`: Marital status indicator.
  - `Purchase`: The total purchase amount (Target Variable).

## Objectives

- Clean and preprocess the retail dataset for analysis.
- Conduct Exploratory Data Analysis (EDA) to find patterns in spending across demographics.
- Formulate and test statistical hypotheses regarding:
  - Average purchase amounts for specific age and gender demographics.
  - Comparing spending behavior between men and women.
  - Analyzing the proportion of high-value customers.

## Methods and Analysis

The notebook follows a structured statistical workflow:

- **Data Cleaning and Preparation**
  - Handling missing values in `Product_Category` columns.
  - Standardizing the `Stay_In_Current_City_Years` column by converting '4+' to numeric values.
  - Encoding categorical variables (Gender, Age, City Category) for statistical processing.

- **Exploratory Data Analysis (EDA)**
  - Summary statistics for purchase amounts.
  - Shape and info inspection to understand data distribution and types.

- **Hypothesis Testing**
  - **One-Sample T-Test:** Testing if the average purchase amount for men aged 18–25 is equal to 10,000.
  - **Two-Sample Independent T-Test:** Comparing the mean purchase amounts between male and female customers to check for significant differences.
  - **Proportions Z-Test:** Checking if the proportion of male customers in the dataset matches a specific population claim (e.g., 75%).
  - **Decision Rule:** Using a significance level of $\alpha = 0.05$ to reject or fail to reject the Null Hypothesis ($H_0$) based on calculated p-values.

## Tech Stack

- **Language:** Python 3
- **Libraries:**
  - `pandas` and `numpy`: For data manipulation and cleaning.
  - `scipy.stats`: For performing T-tests and statistical distributions.
  - `statsmodels`: For proportion-based Z-testing.
- **Environment:** Jupyter / Google Colab

## How to Run

1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/customer-purchase-analysis.git
   cd customer-purchase-analysis

2. *Create and activate a virtual environment (optional but recommended):*
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate

3. *Install dependencies:*
   pip install pandas numpy scipy statsmodels

4. *Open the notebook:*
   jupyter notebook "11_case_study_Purchase amount analysis and hypothesis testing.ipynb"
