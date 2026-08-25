# Customer Shopping Behaviour Analysis

## Overview
Analysis of 3,900 customer shopping transactions to uncover purchasing patterns, spending trends, and customer segments — using SQL for querying, Python for exploration, and Power BI for visualization.

## Business Problem
Retailers need to understand how customers shop — what drives repeat purchases, which segments spend the most, and where revenue is concentrated — to make better marketing and inventory decisions. This project explores those questions using a customer shopping dataset (3,900 rows, 18 columns).

## Tools Used
- SQL (PostgreSQL) — data querying and analysis
- Python (Jupyter Notebook) — data cleaning, feature engineering
- Power BI — interactive dashboard

## Approach
1. **Data Cleaning & Feature Engineering** — `Customer_Shopping_Behaviour_Analysis.ipynb`
   - Imputed 37 missing `Review Rating` values using category-level medians
   - Standardized columns to snake_case
   - Engineered `age_group` and `purchase_frequency_days`
   - Dropped redundant `promo_code_used` column
   - Loaded cleaned data into PostgreSQL
2. **SQL Analysis** — `customer_behaviour.sql`
3. **Dashboard** — `customer_behaviour_dashboard.pbix`
4. **Report** — `Customer Shopping Behavior Analysis.pdf`

## Key Insights
- **Male customers generated over 2x the revenue of female customers** ($157,890 vs. $75,191), despite a fairly even customer base
- **80% of customers are "Loyal"** (3,116 of 3,900) based on purchase history, with only 83 classified as brand-new
- **Subscription status has little effect on individual spend** — subscribers average $59.49 per order vs. $59.87 for non-subscribers — but only 27% of customers are subscribed, leaving revenue upside on the table
- **Discounting is concentrated in a few categories** — Hats have the highest discount dependency at 50%, followed by Sneakers (49.7%) and Coats (49.1%)
- **Revenue is broadly even across age groups**, with Young Adults leading slightly ($62,143) and Seniors lowest ($55,763) — no single age segment dominates
- **Express shipping customers spend more on average** ($60.48) than Standard shipping customers ($58.46)
- **Gloves, Sandals, and Boots have the highest average review ratings** (3.86, 3.84, 3.82), making them strong candidates to feature in marketing

## Business Recommendations
- **Boost subscriptions** — promote exclusive perks, since subscribers currently make up only 27% of the customer base
- **Loyalty programs** — reward repeat buyers to convert "Returning" customers (701) into "Loyal" status
- **Review discount policy** — high discount-dependency on categories like Hats and Sneakers may be eroding margin
- **Feature top-rated products** (Gloves, Sandals, Boots) in campaigns
- **Target high-revenue segments** — Young Adults and Express-shipping customers show stronger spend

## Dashboard Preview
![Customer Behaviour Dashboard](images/dashboard_overview.png)

The dashboard includes filters for Subscription Status, Gender, Category, and Shipping Type, with KPIs for customer count, average purchase amount, and average review rating, plus breakdowns of revenue/sales by category and age group.

## Files in this Repo
| File | Description |
|---|---|
| `Customer_Shopping_Behaviour_Analysis.ipynb` | Python notebook — data cleaning & feature engineering |
| `customer_behaviour.sql` | SQL queries used for analysis |
| `customer_behaviour_dashboard.pbix` | Power BI dashboard |
| `customer_shopping_behavior.csv` | Raw dataset |
| `images/dashboard_overview.png` | Dashboard screenshot |
| `Customer Shopping Behavior Analysis.pdf` | Summary report |

## How to Run
1. Clone this repository
2. Open `Customer_Shopping_Behaviour_Analysis.ipynb` to view the Python cleaning/feature engineering steps
3. Run `customer_behaviour.sql` against the cleaned data (loaded into PostgreSQL/SQL Server)
4. Open `customer_behaviour_dashboard.pbix` in Power BI Desktop to explore the dashboard

## Author
Pavan Purohit
