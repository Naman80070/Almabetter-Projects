# Paisabazaar Credit Score Classification — EDA

## 📌 Project Overview

**Paisabazaar** is a financial services company that helps customers discover and apply for banking and credit products such as loans and credit cards. A key part of their service involves assessing customer **creditworthiness**, since a person's credit score directly influences loan approvals, interest rates, and overall lending risk.

This project performs a structured **Exploratory Data Analysis (EDA)** on customer financial and behavioral data to understand what factors drive a customer's credit score category (`Poor`, `Standard`, `Good`). The insights generated here can help Paisabazaar's risk and product teams make better lending decisions, reduce default risk, and offer more personalized financial product recommendations.

---

## 🎯 Objective

- Understand the structure and quality of the dataset.
- Clean and preprocess the data (handle data type issues, feature engineering).
- Perform Univariate, Bivariate, and Multivariate analysis (**UBM Rule**) using 25+ meaningful charts.
- Extract actionable business insights and recommendations for Paisabazaar's credit risk strategy.

---

## 🗂️ Dataset Description

The dataset contains **100,000 records** across **12,500 unique customers**, with 8 monthly records per customer, covering:

| Category | Features |
|---|---|
| Demographics | Age, Occupation |
| Income | Annual Income, Monthly In-hand Salary |
| Credit & Loan Behavior | Num of Bank Accounts, Credit Cards, Loans, Interest Rate, Credit Mix, Outstanding Debt, Credit Utilization Ratio |
| Payment Behavior | Payment of Min Amount, Payment Behaviour, Delayed Payments, EMI, Monthly Balance |
| **Target Variable** | `Credit_Score` (Poor / Standard / Good) |

---

## 🛠️ Tools & Libraries Used

- **Pandas** — data manipulation, cleaning, and analysis
- **NumPy** — numerical computations
- **Matplotlib** — static visualizations
- **Seaborn** — statistical visualizations
- **Plotly** — interactive visualizations

---

## 🧹 Data Manipulations Performed

- Checked for missing values and duplicate rows (dataset was clean — no nulls or duplicates found).
- Converted incorrectly typed columns (e.g., `Age`, `Num_Bank_Accounts`, `Interest_Rate`) from `float` to `int`.
- Engineered a new feature, `Num_Loan_Types`, by parsing the `Type_of_Loan` column.
- Removed non-analytical identifier columns (`ID`, `Customer_ID`, `Name`, `SSN`).
- Ordered the target variable (`Credit_Score`) logically as `Poor → Standard → Good` for consistent visualization.

---

## 📊 Exploratory Data Analysis (UBM Rule)

The analysis follows a structured approach:
- **U**nivariate Analysis — distribution of individual features
- **B**ivariate Analysis — Numerical-Categorical, Numerical-Numerical, Categorical-Categorical relationships
- **M**ultivariate Analysis — interactions across 3+ variables

15+ charts were created, each accompanied by:
- Why the chart was chosen
- Key insight(s) found
- Business impact (positive or negative, with justification)

---

## 🔑 Key Insights

- **Income, Credit Mix, and Payment Delay** are the strongest indicators of credit score category.
- Customers who **pay only the minimum amount due**, carry **high outstanding debt**, or show **frequent credit inquiries + payment delays** form a clear high-risk group.
- **Occupation alone is a weak predictor** — credit score distribution is fairly similar across professions.
- The dataset shows **class imbalance**, with far fewer "Good" score customers than "Standard" or "Poor."
- The income–credit score relationship **holds consistently across all occupations**.

---

## 💡 Business Recommendations

1. Prioritize **Income, Credit Mix, and Payment Delay** as core risk-screening factors.
2. Build an **early-warning system** for customers showing minimum-payment behavior or rising payment delays.
3. Offer **debt restructuring/consolidation** to the high-debt, high-interest "debt trap" segment instead of outright rejection.
4. Avoid using **occupation** as a risk-screening criterion.
5. Design **tiered credit products** for different income bands.
6. Support **younger customers** with credit-building products and financial literacy resources.
7. Address **class imbalance** before building any future predictive model.

---

## 📁 Repository Structure

```
├── Paisabazaar_Credit_Score_EDA.ipynb   # Main EDA notebook
├── dataset.csv                          # Dataset (if included)
└── README.md                            # Project documentation
```

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Naman80070/Almabetter-Projects.git
   ```
2. Open `Paisabazaar_Credit_Score_EDA.ipynb` in **Jupyter Notebook**, **Google Colab**, or **VS Code**.
3. If using Google Colab, update the dataset file path (via direct upload or Google Drive mount).
4. Run all cells sequentially — the notebook executes end-to-end without errors.

---

## ✅ Conclusion

This project explores Paisabazaar's customer data to understand the key factors influencing credit score classification. Through systematic data cleaning and 25+ visualizations following the UBM rule, it identifies **income, credit mix, and payment delay** as the strongest predictors of creditworthiness, while highlighting a clear high-risk customer segment. These insights lay the foundation for future predictive modeling and more informed, data-driven credit risk decisions at Paisabazaar.

---

## 👤 Author

*Naman Jaju*
*AlmaBetter Data Science Fellowship Program*
