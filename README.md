# Olist E-commerce Sales Analysis (SQL)

SQL analysis of a Brazilian e-commerce dataset. The CSV files are loaded into an in-memory SQLite database from Pandas, then queried with SQL.

**Data:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle). The files are not included here, download them from Kaggle. Tables used: orders, order items, customers.

## Queries

| Question | SQL features |
|---|---|
| Top 5 cities by revenue and average value | JOIN, GROUP BY, ORDER BY, LIMIT |
| Month-over-month revenue growth | CTE, LAG window function |
| Customer spending tiers | CTE, NTILE window function |

## Results

- **Sao Paulo** leads with about **1.86M** in revenue from 15,045 delivered orders, followed by Rio de Janeiro (about 0.96M)
- Monthly revenue grows from the end of 2016 to around 900K per month in 2018

## Limitations and next steps

- Early months of 2016 have very small revenue, so their growth percentages are extreme and should be excluded
- `avg_order_value` is currently the average item price, not the average order value
- `customer_id` in this dataset is created per order, so `customer_unique_id` should be used to analyse real customers

## How this was built

This is a learning project. I built it with help from an AI assistant and studied the code. The notebook comments and chart titles are partly in Azerbaijani.

## Author

Ali Karimov | [LinkedIn](https://www.linkedin.com/in/ali-karimov-505409367)
