# FinSight Bank: NPA Prediction & Credit Risk Modelling

## Overview

This project focuses on analyzing loan portfolios and predicting credit risk for FinSight Bank using advanced data analytics techniques. The objective is to identify high-risk borrowers, estimate Loss Given Default (LGD), and provide data-driven recommendations to improve lending decisions and reduce Non-Performing Assets (NPAs).

The project follows the CRISP-DM methodology and includes:

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Credit Risk Analysis
- LGD Regression Modelling
- Business Recommendations
- Model Evaluation & Diagnostics

---

## Business Problem

FinSight Bank currently relies heavily on rule-based lending decisions, primarily using CIBIL score cutoffs.

This approach ignores numerous risk signals such as:

- Income stability
- Debt burden
- Credit utilization
- Delinquency history
- Macroeconomic indicators
- Loan purpose
- Regional economic factors

The goal is to build a data-driven framework that improves default prediction and minimizes credit losses. :contentReference[oaicite:1]{index=1}

---

## Project Objectives

### 1. Portfolio Analysis
Analyze loan portfolio characteristics and identify data quality issues.

### 2. Risk Signal Identification
Determine which borrower attributes are most associated with default.

### 3. Loss Given Default (LGD) Modelling
Estimate expected losses for defaulted loans.

### 4. Business Strategy Development
Generate actionable recommendations for:

- Underwriting
- Risk-based pricing
- Portfolio monitoring
- NPA reduction

---

## Dataset Information

### Dataset Statistics

| Metric | Value |
|----------|----------|
| Loan Records | 2,000,000+ |
| Source Tables | 9 |
| Features | 171 |
| Time Period | 2010–2024 |
| Dataset Size | 2.02 GB |

### Data Sources

1. Loan Applications
2. Customer Bureau
3. Payment History
4. Loan Performance
5. EMI Tracking
6. Collateral Assets
7. Branch & Economy
8. Credit Card Behaviour
9. Loan Enquiry Bureau

All tables are joined using:

```python
loan_id
```

---

## Project Architecture

```text
Raw CSV Files
       │
       ▼
Data Cleaning
       │
       ▼
Data Integration
       │
       ▼
Feature Engineering
       │
       ▼
Exploratory Data Analysis
       │
       ▼
Regression Modelling
       │
       ▼
Model Evaluation
       │
       ▼
Business Recommendations
```

---

## Tech Stack

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Statsmodels
- SciPy

### Environment

- Jupyter Notebook
- VS Code

---

## Data Cleaning

The dataset contains multiple real-world banking data issues:

### Issues Handled

- Negative Interest Rates
- Zero Income Records
- Invalid DTI Values
- Negative Credit Utilization
- Missing Delinquency Information
- Missing Mortgage Accounts
- Missing Employment Length
- Missing Installment Loan Utilization

### Cleaning Techniques

- Median Imputation
- KNN Imputation
- Mode Imputation
- Sentinel Values
- Winsorization
- Data Validation

---

## Feature Engineering

### Engineered Features

| Feature | Description |
|-----------|-------------|
| emi_to_income_ratio | Monthly repayment burden |
| loan_to_income_ratio | Borrower leverage |
| rate_spread_pct | Loan rate - Repo rate |
| real_interest_rate | Interest rate adjusted for inflation |
| credit_util_composite | Composite utilization score |
| delinq_severity_score | Delinquency severity indicator |
| income_stability_ratio | Income stability measure |
| credit_depth_score | Credit history depth |
| collateral_coverage_ratio | Asset coverage ratio |
| log_annual_inc | Log transformed income |
| log_loan_amnt | Log transformed loan amount |
| enq_velocity_score | Credit enquiry velocity |

---

## Exploratory Data Analysis

### Key Visualizations

- Default Rate Distribution
- CIBIL Score Distribution
- Numerical Feature Histograms
- Correlation Heatmap
- Loan Grade Risk Analysis
- Loan Purpose Default Analysis
- State-wise Default Rates
- COVID-19 Impact Analysis
- Repo Rate vs Default Rate
- LGD Distribution
- CIBIL vs LGD Relationship

---

## Models Used

### Baseline Model

- Ordinary Least Squares (OLS)

### Regularized Models

- Ridge Regression
- LASSO Regression
- Elastic Net Regression

### Model Selection

Hyperparameter tuning performed using:

```python
GridSearchCV
```

---

## Evaluation Metrics

### Classification Metrics

- AUC-ROC
- Gini Coefficient
- False Negative Rate

### Regression Metrics

- R² Score
- Adjusted R²
- RMSE
- MAE

### Diagnostic Tests

- Residual Analysis
- QQ Plot
- Scale-Location Plot
- Cook's Distance
- Variance Inflation Factor (VIF)

---

## Key Business Insights

### Risky Loan Segments

- Grade E-G borrowers exhibit significantly higher default rates.
- Small business loans contribute disproportionately to NPA value.
- Revolving utilization above 80% is a strong early warning indicator.

### Financial Behavior Signals

- Multiple EMI bounces strongly predict future default.
- High enquiry velocity indicates borrower distress.
- Higher collateral coverage significantly reduces LGD.

### Macroeconomic Impact

- COVID-19 created a structural break in default behavior.
- Interest rate cycles materially affect repayment performance.

---

## Business Recommendations

### 1. Redesign Credit Approval Strategy
Move beyond a fixed CIBIL threshold and adopt a multi-factor risk model.

### 2. Segment High-Risk Grades
Apply stricter underwriting policies for Grade E-G borrowers.

### 3. Introduce Early Warning Systems
Monitor EMI bounce patterns and credit utilization changes.

### 4. Create Specialized MSME Scorecards
Use separate risk models for small business lending.

### 5. Enhance Collateral-Based Lending
Improve recovery outcomes through stronger collateral coverage requirements.

---

## Project Structure

```text
FinSight-NPA-Prediction/
│
├── data/
│   ├── raw/
│   ├── processed/
│
├── notebooks/
│   ├── EDA.ipynb
│   ├── Feature_Engineering.ipynb
│   ├── Modeling.ipynb
│
├── reports/
│   ├── figures/
│   ├── final_report.pdf
│
├── src/
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── modeling.py
│   ├── evaluation.py
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Results

| Metric | Target |
|----------|----------|
| AUC-ROC | ≥ 0.82 |
| RMSE | ≤ 8% |
| Gini Coefficient | ≥ 0.64 |
| False Negative Rate | ≤ 15% |

---

## Learning Outcomes

- Credit Risk Analytics
- Banking Domain Knowledge
- Feature Engineering
- Statistical Modelling
- Regression Analysis
- Business Intelligence
- Financial Risk Management
- Data Cleaning at Scale
- CRISP-DM Methodology

---

## Future Improvements

- XGBoost & LightGBM Models
- Probability of Default (PD) Scorecards
- SHAP Explainability
- Real-time Risk Monitoring Dashboard
- Loan Approval Recommendation System

---

## Author

**Kaustubh Indulkar**

PGCP-BDA | C-DAC Mumbai

---

> Think Like a Banker. Analyze Like a Scientist.
