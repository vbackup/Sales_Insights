# Sales Insights Data Analysis Project
## Problem Statement
Create Dashboard to gether insights and increase sales in next quarter.
## Power BI Dashboard
1. Key Insights
![key insights](https://github.com/shuklaharsh3009/sales-insigths/assets/100336788/a38979f4-6d1f-4662-bc1d-a4c51d0dcb67)

2. Profit Analysis
![Profit Analysis](https://github.com/shuklaharsh3009/sales-insigths/assets/100336788/589452bd-cd6f-41f0-9612-89df0b457c91)

3. Performance Insights
![performance insights](https://github.com/shuklaharsh3009/sales-insigths/assets/100336788/4024c0d8-bf02-4883-8e25-e911121c8a8a)

 
### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show district product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

