# Loan-Interest-Rate-Prediction


## Overview
Welcome to the **Loan Interest Rate Prediction** project! In this project, I have aimed to analyze and predict loan interest rates based on various customer and loan-related features. By understanding key factors such as income, loan amount, employment stability and education level, I strive to help financial institutions offer more personalized, fair and efficient loan terms for customers.

**The ultimate goal is to create a predictive model that estimates the loan interest rate, helping financial institutions make better decisions and offer more tailored loan conditions.**

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Steps Involved](#steps-involved)
    - [Data Loading and Cleaning](#data-loading-and-cleaning)
    - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    - [Building Predictive Models](#building-predictive-models)
- [Key Findings](#key-findings)
- [How to Run](#how-to-run)

---

## Introduction
Loan interest rates play a significant role in determining the affordability of loans. However, many factors, such as a borrower’s income, loan amount, and even their previous borrowing history can influence the rates offered. In this project, I have used the **Bondora P2P Loans dataset** to build a model that predicts interest rates based on various borrower characteristics.

**Ultimately, we hope to create a system that predicts fair and accurate interest rates for future applicants.**

---

## Dataset
The dataset used in this project contains several features that describe both the borrower and their loan application:

- **LoanId**: Unique identifier for each loan.
- **Age**: Age of the borrower (years).
- **IncomeTotal**: Total income of the borrower.
- **AppliedAmount**: The loan amount applied for.
- **Amount**: The loan amount actually received by the borrower.
- **Interest**: Interest rate applied to the loan.
- **LoanDuration**: Duration of the loan (in months).
- **Education**: Education level of the borrower (e.g. High School, Bachelor's, etc).
- **EmploymentDurationCurrentEmployer**: Length of time the borrower has been employed at their current job.
- **HomeOwnershipType**: Type of home ownership (e.g. Own, Rent).
- **ExistingLiabilities**: Existing liabilities of the borrower.
- **DebtToIncome**: Ratio of debt to income, calculated as Amount/IncomeTotal.
- **Rating**: Bondora rating assigned to the borrower based on their creditworthiness.
- **PreviousLoans**: Number and value of previous loans before the current one.

---

## Steps Involved

### Data Loading and Cleaning
We start by importing the dataset and performing some basic cleaning steps:
1. **Loading the data** into a Pandas DataFrame.
2. **Handling missing values** by filling or dropping them.
3. **Setting the LoanId** as the index for easy access to individual loans.

---

### Exploratory Data Analysis (EDA)
Next, I have explored the data to understand key patterns and relationships:
- **Descriptive Statistics**: To compute basic statistics (mean, standard deviation, etc.) for key variables like Interest Rate.
- **Risk Identification**: To identify high-risk borrowers based on their debt-to-income ratio and job stability (i.e. borrowers with a DebtToIncome ratio greater than 0.35 and employment duration less than 1 year).
- **Visualizations**: I used box plots to explore how interest rates vary across education levels and scatter plots to examine correlations between numerical features and interest rates.

---

### Building Predictive Models
1. **Simple Linear Regression**: I started with a simple model using just one feature "**AmountOfPreviousLoansBeforeLoan**" to predict interest rates.
2. **Multiple Linear Regression**: After seeing the limitations of the simple model, we expand it to include multiple features, such as **Age**, **Education**, **Income**, and **Loan Amount**. We also handle categorical variables using dummy encoding.
---

## Key Findings
Throughout the analysis, we uncovered some interesting insights:
- **High-Risk Customers**: Borrowers with a DebtToIncome ratio above 0.35 and less than 1 year of employment tend to be high-risk. These customers usually have higher interest rates.
- **Education**: Borrowers with higher levels of education generally receive lower interest rates. This trend was evident in our box plots.
- **Loan Approval**: A significant number of borrowers received less than the amount they applied for. We estimated this issue using a 95% confidence interval, showing that it might be a crucial point to address.

---

## How to Run
To run this project on your local machine, follow these steps:

1. **Clone this repository**:

   ```bash
   git clone https://github.com/your-username/loan-interest-rate-prediction.git
   cd loan-interest-rate-prediction

2. Install the required libraries:

```bash
pip install -r requirements.txt
```
3. Run the analysis and model training:
```bash
jupyter notebook Loan_Interest_Rate_Prediction.ipynb

