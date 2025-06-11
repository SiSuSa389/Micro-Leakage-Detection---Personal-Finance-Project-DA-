# 💸 Micro Leakage Detection and Personal Finance Analysis

This repository contains the code, data, and documentation for a **personal finance project** focused on identifying and analyzing _micro leakage_ — small, often unnoticed expenses that accumulate into significant financial inefficiencies 💰. The solution leverages **Python (ML & EDA)**, **SQL**, and **Power BI** to uncover hidden financial patterns and provide actionable insights.

---

## 📚 Table of Contents (Detailed walkthrough in the Report)

1. [Executive Summary](#1-executive-summary)
2. [Problem Statement](#2-problem-statement)
3. [Data Overview](#3-data-overview)
4. [Methodology & Workflow Overview](#4-methodology--workflow-overview)
5. [Exploratory Data Analysis (Python)](#5-exploratory-data-analysis-python)
6. [Machine Learning Model](#6-machine-learning-model)
7. [SQL-Based Analysis](#7-sql-based-analysis)
8. [Power BI Dashboard](#8-power-bi-dashboard)
9. [Final Business Insights](#9-final-business-insights)
10. [Challenges & Learnings](#10-challenges--learnings)
11. [Future Scope](#11-future-scope)
12. [Tools & Technologies Used](#12-tools--technologies-used)
13. [Repository Structure](#13-repository-structure)
14. [Appendix](#14-appendix)

---

## 1. 🧾 Executive Summary

This project tackles the issue of **financial micro leakage**—tiny, habitual, and easily-overlooked expenses like impulse buys or unused subscriptions. Over time, these add up and hinder financial progress.

By transforming raw transaction data into rich insights, the project provides a comprehensive analysis pipeline:
- 📊 **EDA in Python**
- 🤖 **ML model** to classify transactions as leakage or not
- 🧮 **SQL** for business analysis
- 📈 **Power BI dashboard** to visualize income, expenses, and savings

🔍 **Key Insight**: ~4–5% of all transactions were classified as leakage, with common culprits being **Dining Out**, **Medical**, and **Fuel**.

---

## 2. ❓ Problem Statement

### What is Micro Leakage?

Micro leakage refers to small, unnoticed, or recurring financial outflows that silently drain your resources — like unused streaming subscriptions, snacks, or minor impulsive purchases.

### Why Detect It?

✅ Improves savings  
✅ Boosts financial clarity  
✅ Enables smarter budgeting

### Project Objective

Implement a 3-layered solution:

- ✅ **ML Classification** to label transactions
- ✅ **SQL Analysis** to dig deeper
- ✅ **Power BI Dashboard** for intuitive decision-making

---

## 3. 📂 Data Overview

The dataset is **synthetic** but designed to reflect real-world spending behavior.

### 🔑 Key Columns:

- `timestamp`, `type`, `category`, `value`
- `is_necessary`, `payment_mode`, `is_recurring`
- `context`, `time_block`, `day_type`
- `cumulative_monthly_spend`

🧾 1000+ rows of transactions covering diverse categories and time periods.

---

## 4. ⚙️ Methodology & Workflow Overview

1. 🧪 **Data Simulation**  
2. 📊 **Python EDA & Preprocessing**  
3. 🤖 **Machine Learning Model**  
4. 🔍 **SQL Queries** for business insights  
5. 📈 **Power BI Dashboard** for monthly tracking

Each layer adds a new perspective to the financial picture.

---

## 5. 🐍 Exploratory Data Analysis (Python)

📌 **Findings:**

- "Others" category (28.2%) likely masks leakages
- High transaction count in ₹200–₹300 range 🚨
- Subscriptions and mobile recharges are common culprits
- Leakage patterns seen mostly in **evenings**, **weekdays**
- Dining out leads the leakage leaderboard
- Morning/evening + unplanned expenses = 🔥 leakage hotspots
- Monthly trends show spikes in **May, July (2023)** and **Jan, May (2024)**

---

## 6. 🤖 Machine Learning Model

- 🧠 **Task**: Binary classification (`is_leakage`)
- 🔍 **Models**: Logistic Regression, Random Forest, XGBoost
- 🏆 **Best Model**: Random Forest (highest F1-score)
- ✅ Zero false positives/negatives in test data
- ⚠️ Slight overfitting observed (can be fixed with more data)

---

## 7. 🧮 SQL-Based Analysis

After ML classification, SQL helped answer 🔍 key business questions:

- Total spend/month in 2023  
- Most common expense categories  
- Average value: recurring vs non-recurring  
- Leakage by context (e.g., Emergency, Festive)  
- 📆 Day with highest spend: **Sunday**  
- ⏰ Top leakage time blocks: Evening > Night > Morning  
- 💳 Debit Card showed the **highest leakage score** on average  
- 🎯 Cutting top 10% leakage expenses in half boosts savings

---

## 8. 📊 Power BI Dashboard

An interactive dashboard for **monthly finance tracking**:

### 🔢 KPIs:
- Income, Expenses, Savings, Savings %, MoM changes

### 📈 Visuals:
- Category breakdowns (e.g., Rent, EMI, Dining)
- Savings split (Liquid Cash, FD, Emergency)

### 💡 Use Case:
Perfect for **personal budgeting** and **financial self-awareness**.

---

## 9. 💡 Final Business Insights

- ⚠️ 4-5% of transactions are micro leakage
- 🍽️ Top leakage sources: Dining Out, Medical, Fuel
- ⏰ Leakage spikes in evenings/weekdays
- 💳 UPI, Debit Card & Net Banking dominate micro spends
- 📆 Post-salary dates show leakage surges

---

## 10. 🧠 Challenges & Learnings

- 🎯 Defining "leakage" needed custom scoring logic
- ⚖️ Class imbalance required careful evaluation
- 🧪 Overfitting needed mitigation through validation

---

## 11. 🚀 Future Scope

- 🛎️ Automated alerts for suspicious leakages
- 🌐 Real-time data tracking
- 💼 Extend to corporate finance datasets

---

## 12. 🛠️ Tools & Technologies Used

| Tool        | Usage                                   |
|-------------|------------------------------------------|
| 🐍 Python   | EDA, ML modeling (pandas, sklearn, etc.) |
| 🧮 SQL      | Business insights and queries            |
| 📊 Power BI | Dashboard for visualization              |
| 💻 GitHub   | Code versioning and collaboration        |

---

## 13. 🗂 Repository Structure

```
/Project-Root
│
├── Notebooks/
│   └── micro_leakage_analysis.ipynb  # Python notebook
├── SQL/
│   └── main_sql_queries.sql           # SQL scripts
├── Dashboard/
│   └── personal_finance_dashboard.pbix
├── Data/
│   ├── raw_dataset.csv
│   └── cleaned_dataset.csv
├── Report/
│   └── Final_Report.pdf
├── README.md
```

---

## 14. 📎 Appendix

- 🧪 The dataset was synthetically generated to simulate real-life scenarios.
- 📁 For privacy, no real financial data is used.

---

### 📬 Feedback & Contributions

Feel free to raise issues or contribute enhancements to this repo! Pull requests are welcome 🙌

