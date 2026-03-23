# CIND 820 Capstone: Post-Default Recovery Optimization 📉💡
**Predicting Collection Outcomes in Unsecured Lending**

**Author:** Syed Muzammil Iqbal  
**Course:** CIND 820 - Big Data Analytics Project  
**Supervisor:** Ceni Bobaoglu  

## Project Overview
In the domain of unsecured consumer lending, the "Charged Off" status represents a critical financial loss event. Traditional credit risk modeling focuses heavily on the Probability of Default (PD), often treating the subsequent recovery process as a static outcome. When Loss Given Default (LGD) is modeled, it typically predicts *gross* recovery, ignoring the significant operational costs and contingency fees associated with third-party collections. 

This project addresses that operational inefficiency by engineering a `Net_Recovery` target variable and developing predictive models to help lenders triage defaulted accounts. By predicting net yield and clustering borrowers into strategic "Recovery Personas," lenders can make data-driven decisions on whether to retain debt for internal collection or sell it immediately to third-party debt buyers.

## Dataset Information
* **Source:** [All Lending Club Loan Data (Kaggle)](https://www.kaggle.com/wordsforthewise/lending-club)
* **Timeframe:** 2007 - 2018Q4
* **Scope:** Filtered specifically for loans where `loan_status == 'Charged Off'` (approx. 268,000 records).
* **Note:** Due to GitHub file size limits, the raw dataset is not uploaded to this repository. Please download `accepted_2007_to_2018Q4.csv` from the Kaggle link above to run the code.

* ## Methodology (The 5 Phases)
1. **Data Loading & EDA:** Exploratory analysis identifying the strict contingency fee structure and the target variable problem.
2. **Feature Engineering:** Engineering the `Net_Recovery` target variable to account for collection fees and addressing the severe zero-inflation phenomenon.
3. **Data Cleaning & Preprocessing:** Handling missing values, ordinal encoding for credit grades, and standard scaling.
4. **Predictive Modeling:** Training a Random Forest Regressor to predict net yield at the point of default, extracting feature importances for algorithmic transparency.
5. **Strategic Segmentation:** Applying K-Means clustering to segment borrowers into three distinct, actionable business personas based on yield and risk profiles.

## Key Findings & Strategic Action Plans
* **Persona 0 (High-Yield Whales):** High balances yielding over $3,000. **Action:** Retain internally.
* **Persona 1 (Small-Balance Nuisances):** Tiny loan balances yielding under $500. **Action:** Package and sell immediately as a low-balance portfolio.
* **Persona 2 (Toxic Assets):** Subprime borrowers with severe DTI ratios averaging 24.2. **Action:** Cut losses and sell immediately as a deep-subprime portfolio.

## Repository Contents
```text
├── notebooks/
│   └── Milestone3_InitialResults_Code.ipynb   # Main Google Colab Jupyter Notebook
├── reports/
│   ├── Milestone3_InitialResults_Code.pdf     # Compiled HTML/PDF version of the notebook
│   └── Iqbal_SyedMuzammil_LitReview.docx      # Milestone 2 Literature Review & Methodology
├── README.md                                  # Project overview and instructions
└── requirements.txt                           # Python dependencies for reproducibility
