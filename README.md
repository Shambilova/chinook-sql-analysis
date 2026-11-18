# Chinook Music Store: Sales Analysis with SQL

SQL analysis of an online music store: revenue trends, markets, genres, customer concentration and sales team performance.

**[Open the notebook in Google Colab](https://colab.research.google.com/github/Shambilova/chinook-sql-analysis/blob/main/chinook_sql_analysis.ipynb)**

## Business questions
1. How does revenue change over time (by year, month, season)?
2. Which countries bring the most revenue, and how much does each customer spend?
3. Which genres and artists sell best?
4. How concentrated is the customer base (does a small group bring most of the revenue)?
5. How do the sales reps perform?

## Data
Chinook sample database (SQLite): 59 customers, 412 invoices, 3,503 tracks, invoices from Jan 2021 to Dec 2025.
Source: [lerocha/chinook-database](https://github.com/lerocha/chinook-database). It is a learning database, so the findings describe this dataset, not a real company.

## SQL techniques
`JOIN` (up to 4 tables) · `GROUP BY` · CTEs (`WITH`) · window functions (`LAG`, `SUM() OVER`, `NTILE`) · date functions (`strftime`)

## Key findings
- **Revenue is stable:** $449-481 per year, about 83 invoices a year. No strong seasonality (weakest and strongest month differ by about 8%).
- **Markets:** USA 22.5% and Canada 13.1% of revenue; top 5 countries about 59%. Revenue per customer is similar across countries ($38-40), so markets differ mainly by number of customers.
- **Products:** Rock is 35.5% of revenue; the top 4 genres give about 73.5%. TV content sells at $1.99 per unit versus $0.99 for music.
- **Customers:** the top 10% of customers bring only 12% of revenue, so the business does not depend on a few key customers.
- **Sales team:** differences in rep revenue come from portfolio size (18-21 customers), not from revenue per customer.

## Charts

![Revenue by year](images/revenue_by_year.png)

![Monthly revenue and seasonality](images/monthly_revenue.png)

![Countries](images/countries.png)

![Genres and artists](images/genres_artists.png)

![Customer deciles](images/customer_deciles.png)

![Sales reps](images/sales_reps.png)

## Stack
SQL (SQLite), Python, pandas, Matplotlib, Google Colab.

## How to run
Open the notebook in Google Colab and choose Runtime → Run all. The database is downloaded automatically.
