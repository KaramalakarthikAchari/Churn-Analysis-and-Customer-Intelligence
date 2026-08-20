Customer Churn Analysis — OTT Subscription Data

An end-to-end churn analytics project built with Python, Pandas, SQLite, Matplotlib, and Seaborn, analyzing subscriber behavior for a hypothetical OTT streaming platform to figure out who's likely to leave, why, and what it's costing the business.

The Problem

In subscription businesses (streaming, SaaS, telecom), retaining an existing customer is far cheaper than acquiring a new one. This project treats churn like a real business problem — pulling data from three relational tables (customer demographics, subscription details, and support interactions), cleaning it, and turning it into numbers a growth or retention team could actually act on.

Dataset

Data was stored in a SQLite database (customer_churn.db) across three tables:

db_customer — customer demographics (country, state, gender, DOB)
db_subscription — plan type, contract type, billing, cancellation info, churn score
db_support — complaints, escalations, CSAT scores

What I Did
Connected Python to SQL — pulled all three tables using sqlite3 + pandas
Cleaned the data — fixed column names, handled missing values, standardized inconsistent categories (e.g. gender labels), converted date columns
Merged the tables into a single analysis-ready dataframe on customerid
Engineered features — churn flag, customer age, subscription tenure, complaint counts, churn risk buckets (low/med/high)
Ran the analysis — churn rate, retention rate, ARPU, revenue at risk, churn by plan type/state/contract type, complaint-to-churn patterns
Visualized it — churn trends over time, churn rate by plan and by state, a correlation heatmap across key variables

Key Findings
Churn rate: 28.57% | Retention rate: 71.43%
Basic plan subscribers churn the most (60%) vs. Premium (14.3%) — cheaper tiers are the highest flight risk
Monthly contracts churn far more than annual contracts — a strong signal that contract structure drives loyalty
Karnataka showed the highest regional churn, worth digging into for pricing or service issues
Average customer tenure and revenue-at-risk were calculated to size the retention opportunity
Tools  : Python · Pandas · NumPy · SQLite3 · Matplotlib · Seaborn
