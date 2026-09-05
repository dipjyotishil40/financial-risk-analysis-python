# 💰 Financial Risk Analysis with Python

## 📌 Project Overview

This project analyzes financial transaction data using Python to identify customer behaviour, account activity patterns, potential financial risks, and relationships between transaction activity and account balances.

The analysis was performed using Python, Pandas, Matplotlib, and statistical analysis techniques on a dataset containing **800 financial transaction records and 15 variables**.

The project focuses on transforming transaction-level data into meaningful account-level insights that can support customer segmentation, risk monitoring, anomaly identification, and financial decision-making.

---

## 🎯 Objectives

- Clean and prepare financial transaction data for analysis
- Analyze transaction patterns and financial activity
- Identify high- and low-performing accounts
- Build customer profiles based on activity, balance, and transaction volume
- Identify potential financial-risk indicators
- Detect unusual withdrawal and balance behaviour
- Create meaningful visualizations
- Perform statistical hypothesis testing
- Provide data-backed business recommendations

---

## 📊 Dataset

The dataset contains **800 transaction records** covering the period from **2023 to June 2024**.

### Key Variables

- Transaction ID
- Customer ID
- Account ID
- Account Type
- Transaction Type
- Product
- Firm
- Region
- Manager
- Transaction Date
- Transaction Amount
- Account Balance
- Risk Score
- Credit Rating
- Tenure Months

### Transaction Types

- Withdrawal
- Payment
- Deposit
- Transfer

---

## 🔎 Analysis Performed

### 1. Data Cleaning and Formatting

- Checked dataset structure and data types
- Checked for missing values
- Examined numerical distributions
- Standardized financial data for analysis
- Validated transaction dates and financial fields

### 2. Descriptive Transactional Analysis

- Analyzed transaction activity over time
- Compared credits and debits
- Calculated net financial flow
- Identified top and bottom accounts by net flow
- Analyzed transaction gaps and account activity
- Identified potentially inactive accounts

### 3. Customer Profile Building

- Classified accounts into Low, Medium, and High activity groups
- Segmented customers using average balance and transaction volume
- Identified high-net-inflow accounts
- Identified high-frequency, low-balance accounts
- Identified accounts with negative or near-zero balances

### 4. Financial Risk Identification

- Identified relatively large withdrawals
- Analyzed RiskScore
- Measured balance volatility
- Investigated frequent withdrawal behaviour
- Applied statistical anomaly detection
- Identified accounts requiring further monitoring

### 5. Data Visualization

Created visualizations for:

- Transaction type distribution
- Transaction amount distribution
- Transaction amount by transaction type
- Monthly transaction trends
- Monthly credits vs. debits
- Activity by account type
- Transaction volume by region
- Average transaction amount by region
- Top customers by transaction volume
- Transaction frequency vs. average transaction amount

### 6. Hypothesis Testing

Tested whether high-volume transaction accounts have statistically higher average balances than low-volume transaction accounts.

A one-tailed Welch's independent samples t-test was used.

**Result:**

- P-value: **0.367563**
- Significance level: **0.05**
- Decision: **Fail to reject the null hypothesis**

The analysis did not find statistically significant evidence that high-volume accounts have higher average balances.

---

## ❓ Key Business Questions

This project answers questions such as:

- Which accounts have the highest and lowest net financial flow?
- Which customers are highly active?
- Which accounts maintain high balances?
- Which customers have high transaction frequency but relatively low balances?
- Which accounts have negative balances?
- Which accounts show relatively large withdrawals?
- Which customers demonstrate frequent withdrawal behaviour?
- Which accounts have higher financial-risk indicators?
- Does higher transaction volume imply a higher account balance?
- Which customer groups require additional monitoring or engagement?

---

## 💡 Business Value

The analysis can help financial teams:

- Improve customer segmentation
- Identify accounts requiring additional monitoring
- Detect unusual transaction behaviour
- Monitor negative-balance accounts
- Review relatively large withdrawals
- Identify high-frequency, low-balance customers
- Re-engage low-activity customers
- Combine multiple risk indicators for better risk assessment
- Support data-driven customer and financial decisions

---

## 🔑 Key Findings

- **194 accounts** were identified in the customer profiling analysis.
- **73 accounts** were classified as High Activity, **76 as Medium Activity**, and **45 as Low Activity**.
- The median average balance was **72,044.73**.
- The median transaction volume was **4 transactions**.
- **ACC46655** recorded the highest net flow at approximately **728,037.40**.
- **ACC46953** recorded the lowest observed net flow at approximately **−24,811.43**.
- **ACC19178** had an average balance of approximately **−1,541.18**.
- Two accounts were identified using the 95th-percentile large-withdrawal threshold of approximately **26,975.89**.
- **CUST1962** and **CUST5174** recorded the highest identified withdrawal frequency of **5 withdrawals**.
- Financial risk should not be evaluated using RiskScore alone; multiple indicators provide a stronger view of account behaviour.
- The hypothesis test found no statistically significant evidence that high transaction volume leads to higher average account balances.

---

## 🛡️ Risk Monitoring Approach

The project uses a multi-indicator approach:

**RiskScore + Withdrawal Behaviour + Balance Volatility + Transaction Frequency + NetFlow + Account Balance**

These indicators should be considered together when identifying accounts that may require further investigation.

Importantly, the analysis identifies **potential risk indicators** and does not automatically classify customers or transactions as fraudulent.

---

## 💼 Business Recommendations

1. **Use Multiple Risk Indicators**  
   Combine RiskScore with balance volatility, withdrawals, transaction frequency, NetFlow, and account balance.

2. **Monitor Negative-Balance Accounts**  
   Review accounts with negative average balances to understand possible overdraft or insufficient-fund situations.

3. **Monitor High-Frequency, Low-Balance Accounts**  
   Review unusual cash-flow patterns while considering appropriate customer-engagement opportunities.

4. **Review Large Withdrawals**  
   Investigate relatively large withdrawals together with account history and customer behaviour.

5. **Re-engage Low-Activity Customers**  
   Monitor low-activity accounts and consider suitable customer-retention strategies.

6. **Investigate Repeated Withdrawal Behaviour**  
   Customers with frequent withdrawals can receive additional transaction-level review when multiple risk indicators occur together.

7. **Avoid Overinterpreting Statistical Results**  
   Transaction volume alone should not be used to explain account balances or financial risk.

---

## ⚠️ Analytical Limitations

- The dataset represents a specific observed period and should not automatically be generalized to all customers or future periods.
- RiskScore is treated as an existing dataset variable; this project does not construct or validate the underlying scoring model.
- Statistical outlier detection depends on the selected methodology.
- Dormant/Inactive is an analytical classification based on transaction gaps and does not confirm official banking status.
- Negative/near-zero balance analysis currently uses an average balance of zero or below.
- Statistical significance and business significance are different concepts.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **Matplotlib**
- **Statistical Analysis**
- **Jupyter Notebook**

---

## 📁 Project Structure

```text
financial-risk-analysis-python/
│
├── Financial_Risk_Analysis.ipynb
└── README.md
