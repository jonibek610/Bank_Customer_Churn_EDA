# Bank Customer Churn — Exploratory Data Analysis

Analysis of 10,000 retail bank customers to find out why customers leave and what the bank can do about it.

## Dataset

Source:https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn

Download `Customer-Churn-Records.csv` and place it in the project root before running the notebook.

## Key Findings

**1. Overall churn rate: 20.38%**
1 in 5 customers left the bank. Significant for a retail bank.

**2. Germany churns at 32.4% — double France (16.2%) and Spain (16.7%)**
Fewer customers, but loses 1 in 3 of them. A Germany-specific problem, not a company-wide one.

**3. Churners average 44.8 years old vs 37.4 for customers who stayed**
A 7-year gap. Middle-aged customers leave more.

**4. Inactive members churn at 26.9% vs 14.3% for active members**
Engagement predicts retention.

**5. Customers with 3-4 products churn at 83-100%**
Customers with 2 products churn the least, at 7.6%. Over-selling backfires.

**6. 99.5% of customers who complained churned**
Too clean a correlation to be causal — likely data leakage, since the complaint flag may get logged at the same time as the exit, not before it. Treated as a symptom, not a standalone predictor.

**7. Card type and credit score show no meaningful churn signal**
Churn rates stay flat (19-22%) across all card tiers. Credit score differs by under 6 points between groups.

## Business Recommendations

1. **Germany retention fix** — investigate local competitor pricing and service gaps specific to Germany.
2. **Complaint response time tracking** — flag customers for retention outreach if unresolved past 48 hours, instead of only logging that a complaint happened.
3. **Cross-sell audit** — cap product recommendations at 2 per customer, review whether sales incentives are pushing unnecessary products.
4. **Inactive member re-engagement** — automated triggers (app notifications, offers) for customers inactive 30+ days.
5. **Age-targeted campaigns** — focus retention marketing on the 40-55 age bracket.

## Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn

## How to Run

```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook Bank_Customer_Churn_EDA.ipynb
```
