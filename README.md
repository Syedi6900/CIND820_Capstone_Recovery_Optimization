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

## Repository Contents
```text
├── notebooks/
│   └── Milestone3_InitialResults_Code.ipynb   # Main Google Colab Jupyter Notebook
├── reports/
│   ├── Milestone3_InitialResults_Code.pdf     # Compiled HTML/PDF version of the notebook
│   └── Iqbal_SyedMuzammil_LitReview.docx      # Milestone 2 Literature Review & Methodology
├── README.md                                  # Project overview and instructions
└── requirements.txt                           # Python dependencies for reproducibility
