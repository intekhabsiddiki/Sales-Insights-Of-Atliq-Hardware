# Sales-Insights-Of-Atliq-Hardware

### Sales Report

**Importance of Sales Data Analysis:** Revealing sales trends, monitoring crucial performance metrics, and facilitating well-informed choices

**Reports' Role:** Assessing impactful customer discount strategies, streamlining negotiation processes, and pinpointing growth prospects within potential markets

## Technical & Soft Skills:
-Proficient in ETL methodology (Extract, Transform, Load).
-Creating date tables using Power Query.
-Make Insights of fiscal months and quarters.
-Establishing data model relationships in Power BI.
-Integrating more data into existing data models.
-Skilled in using DAX to create calculated columns.
## Soft Skills:
Comprehensive understanding of Sales Report.
Establishing method for formulating plans for report making.



Steps:

 SQL database dump 

## Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

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


## Data Analysis Using Power BI

 import SQL databse into Power BI

1. Formula to create norm_amount column

`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`

Find the detailed project reports [here](https://github.com/intekhabsiddiki/Sales-Insights-Of-Atliq-Hardware).

