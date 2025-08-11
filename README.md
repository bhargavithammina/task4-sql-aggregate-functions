# Task 4: Aggregate Functions and Grouping


## Objective
Use aggregate functions and grouping to summarize and analyze tabular data in SQL.

## Tools Used
- SQLiteStudio / DB Browser for SQLite
- MySQL Workbench

## Contents
- Task4_Aggregate Functions and Grouping` → SQL script for Task 4  
- `Orders.csv` → Sample dataset for practice  
- `screenshots` → Final output screenshots  
- `README.md` → Project documentation  



## Sample Table: Orders

| OrderID | CustomerName | Product   | Quantity | Price  |
|---------|--------------|-----------|----------|--------|
| 1       | Alice        | Laptop    | 1        | 50000  |
| 2       | Bob          | Mouse     | 2        | 500    |
| 3       | Alice        | Keyboard  | 1        | 1500   |
| 4       | Charlie      | Laptop    | 1        | 48000  |
| 5       | Bob          | Laptop    | 1        | 52000  |

---

##  SQL Queries and Explanations

##  Count total orders

SELECT COUNT(*) AS total_orders FROM Orders;

##  Calculate total revenue

SELECT SUM(Quantity * Price) AS total_revenue FROM Orders;

## Find average price of products

SELECT AVG(Price) AS avg_price FROM Orders;

##  Group total sales by customer

SELECT CustomerName, SUM(Quantity * Price) AS total_sales

FROM Orders

GROUP BY CustomerName;

##  Filter customers with sales above ₹50,000

SELECT CustomerName, SUM(Quantity * Price) AS total_sales

FROM Orders

GROUP BY CustomerName

HAVING total_sales > 50000;

Sample Output:

| Query                        | Output                                      |
| ---------------------------- | ------------------------------------------- |
| Total Orders                 | 5                                           |
| Total Revenue                | 152500                                      |
| Average Price                | 30500                                       |
| Total Sales per Customer     | Alice - 51500, Bob - 53000, Charlie - 48000 |
| Customers with Sales > 50000 | Alice, Bob                                  |

Author
**Name:** Bhargavi Thammina  
**Email:** bhargavithammina@gmail.com  
**LinkedIn:** [linkedin.com/in/bhargavi-thammina-846053263](https://linkedin.com/in/bhargavi-thammina-846053263)  
**GitHub:** [github.com/Bhargavi-Thammina](https://github.com/Bhargavi-Thammina)
---


