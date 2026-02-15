# Post-Default Recovery Optimization: Predicting Collection Outcomes in Unsecured Lending

**Author:** Syed Muzammil Iqbal
**Student ID:** 501410187
**Supervisor:** Ceni Babaoglu
**Course:** CIND 820 Capstone Project 
---
## Project Overview
In unsecured consumer lending, a "Charged Off" status represents a significant financial loss. Traditional recovery strategies often apply uniform resources to defaulted accounts, ignoring the variability in Loss Given Default (LGD). This project aims to optimize the post-default recovery process by focusing on **Net Recovery** (Gross Recoveries minus Collection Fees).

**Research Goal:** To develop a machine learning framework (using Random Forest Regressors and K-Means Clustering) that predicts the profitability of collection efforts and segments borrowers into actionable recovery personas.

## Dataset
The project utilizes the **LendingClub Loan Data (2007–2018)**, sourced from Kaggle.
* **Filter:** The data is filtered to include only loans with `loan_status == 'Charged Off'`.
* **Size:** Approximately 268,000 records.
* **Data Source:** [Link to Kaggle Dataset](https://www.kaggle.com/wordsforthewise/lending-club)
* *Note: Due to size constraints, the raw data file is not included in this repository.*

## Repository Structure
* `notebooks/`: Jupyter notebooks containing exploratory data analysis (EDA), preprocessing steps, and modeling (in progress).
* `data/`: Placeholders for raw and processed data (local use only).

## Methodology Pipeline
1.  **Preprocessing:** Imputing missing delinquency data and engineering the `Net_Recovery` target variable.
2.  **Modeling:** Using Random Forest Regressors to handle non-linear relationships and zero-inflated recovery data.
3.  **Segmentation:** Applying K-Means clustering to define borrower recovery profiles based on fees, DTI, and recovery potential.

---
*Milestone 2 Interim Report Submission*