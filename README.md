# MyProjects
Credit Risk Assessment
RWA & Capital Requirements (Basel III) This project analyzes a dataset of 5,960 home equity loans to estimate Risk-Weighted Assets (RWA) and capital requirements for a bank portfolio in line with the Basel III regulatory framework. Both the Standardised Approach (SA) and the Internal Ratings-Based (IRB) approach are applied.

Dataset Description The dataset contains anonymized loan-level information, including borrower status and financial attributes. Key Columns:

Column	Description
BAD	1 = Defaulted loan / 0 = Non-defaulted loan
MORTDUE	Amount due on existing mortgage
VALUE	Estimated value of the property
JOB	Occupation of borrower (categorical)
YOJ	Years at present job
DEROG	Number of major derogatory credit reports
DELINQ	Number of delinquent credit lines
CLAGE	Age of oldest credit line (in months)
NINQ	Number of recent credit inquiries
CLNO	Number of credit lines
DEBTINC	Debt-to-income ratio
Objective

Calculate Risk-Weighted Assets (RWA) and Capital Requirements for each loan
Compare results between:
Standardised Approach (SA) under Basel III
Foundation Internal Ratings-Based Approach (F-IRB)
Methodology

Data Preprocessing
Fill missing values
Cap outliers in numeric columns
Calculate Loan-to-Value (LTV) = MORTDUE / VALUE
Standardised Approach (SA)
Define risk weights (RW) based on LTV bands
Compute:
RWA = EAD × RW
Capital = RWA × 8%
IRB Approach
Assign Probability of Default (PD), Loss Given Default (LGD), and Exposure at Default (EAD)
Calculate capital requirement (K) using Basel IRB formula
Compute:
RWA = K × 12.5 × EAD
Capital = RWA × 8%
Evaluation
Aggregate and compare total RWA and capital under both approaches
Outputs

ROC Curve & AUC metrics
Capital requirement tables:
CET1 (4.5%)
Tier 1 (6%)
Total Capital (8%)
Tools Used

Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib, Plotly)
Jupyter Notebook
Basel III documentation (CRE31, CRE36)
Files

RiskAnalyticsProject.ipynb – Jupyter notebook with full code
Mortgage_default - hmeq.csv – Main input dataset
README.md – This file
