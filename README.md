 plsql_window_functions_29146_Ihozo-Meg
 
## Project Overview
 
A comprehensive implementation of SQL JOINs and window functions for business analytics in the food and beverage industry. This academic project analyzes coffee shop sales data to understand customer purchasing behavior, identify top-selling drinks by weekday and weekend, and support inventory and promotion decisions using SQL analytical functions.

---

 A. Problem Definition

 1. Company
Small Coffee Shop (Food & Beverage Industry)

2. Department
Sales & Inventory Analytics

3. Business Challenge
The coffee shop records daily sales transactions but does not know which drinks sell the most during weekdays versus weekends. In addition, the shop lacks insight into whether customers usually buy a single item or multiple items per visit. Without this information, it is difficult to plan inventory levels and design effective promotions.

 4. Expected Outcome
Data-driven insights to identify top-selling drinks by day type, understand customer purchasing patterns, optimize inventory stocking, and create targeted weekday and weekend promotions.

---

 B. Database Schema

The database contains three related tables:

 1. customers
- customer_id  
- customer_name  
- visit_date  
- day_type (Weekday / Weekend)

 2. products
- product_id  
- product_name  
- category  
- price  

 3. sales
- sale_id  
- customer_id  
- product_id  
- quantity  
- sale_date  

Relationships
- One customer can make many purchases
- One product can be sold many times
- The sales table connects customers and products

An ER Diagram is included in the repository as a screenshot.

---

SQL JOIN Queries Implemented

 1. INNER JOIN
Retrieves valid sales records with matching customers and products.  
Interpretation: Shows completed transactions and supports accurate sales reporting.

2. LEFT JOIN
Identifies customers who visited the shop but did not make any purchases.  
Interpretation:Helps identify potential customers for promotions.

 3. RIGHT JOIN
Detects products that have never been sold.  
Interpretation: Highlights drinks that may need promotion or removal.

4. FULL OUTER JOIN
Combines all customers and products, including unmatched records.  
Interpretation: Ensures full visibility of all data.

 5. SELF JOIN
Compares customers who visited the shop on the same day.  
Interpretation: Helps identify peak days with high customer traffic.

---

 Window Functions Implemented

1. RANK()
Ranks drinks based on total quantity sold for weekdays and weekends.  
Interpretation: Identifies the most popular drinks depending on the day type.

2. SUM() OVER()
Calculates running totals of daily sales.  
Interpretation: Shows cumulative sales growth over time.

3. LAG()
Compares daily sales with the previous day.  
Interpretation: Helps identify increases or decreases in sales from one day to the next.

 4. NTILE(4)
Segments customers into quartiles based on total items purchased.  
Interpretation: Identifies high-value customers and low-frequency buyers.

---

 Result Analysis

 1. Descriptive (What Happened)
- Weekend sales were higher than weekday sales.
- Some drinks sold significantly more on weekends.
- Most customers purchased more than one item per visit.

 2. Diagnostic (Why It Happened)
- Customers have more free time on weekends, leading to higher consumption.
- Popular drinks are often ordered together with snacks or add-ons.

 3. Prescriptive (What To Do Next)
- Stock more top-selling drinks for weekends.
- Introduce weekday promotions or bundles to increase sales.
- Reward frequent customers with loyalty offers.

---

 References
1. MySQL 8.0 Documentation – Window Functions  
2. PostgreSQL Documentation – Analytical Functions  
3. Course Lecture Notes: Database Development with PL/SQL  
4. SQL Tutorial – Window Functions and JOINs  

---

 All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.”
