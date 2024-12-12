# Database-Development-for-Shoppers-Drug-Marts

Enes Polat, Simon Lin and Dylan Ha

Comprehensive Point of Sale (POS) System for Shopper Drug Marts to optimize retail and pharmacy management, enabling effective inventory control, customer data management, and prescription processing.

- Designed and implemented SQL tables for entities including Employees, Products, Customers, Transactions, Inventory, and Receipts.
- Created advanced queries for data retrieval, including aggregations, joins, and subqueries, enabling insights into inventory levels, customer points, and sales.
- Utilized views to simplify access to specific datasets, such as cashless payments and high-value products.
- Developed functionalities for customer registration, product inventory management, order tracking, and payment processing.
- Implemented functional dependencies to maintain database integrity, ensuring accurate relationships among POS system entities.

Requirements: 
- Python 3
- tkinter (run pip install tk)
- cx_Oracle (run pip install cx_Oracle)
   -note: may require installation of MSVC C++ Build Tools v14.0 or greater
- PIL (Pillow, run pip install pillow, should come with tk installation)

After installing, connect to the CS VPN and execute main.py, logging in with your CS credentials to access the database.

To start fresh, you can drop all existing tables, then select "Create all tables" to initialize the database structure.

"Populate all tables" option fills the tables with sample data for testing purposes.

"Query All Tables" feature runs some predefined advanced queries and displays their results.

"Show all Tables" will display the current tables in the database.

"Run Custom Query" feature lets you enter and execute a valid SQL query directly in the input field.

"Drop all Tables" option removes all database tables.

"Exit" closes the application.

Below are examples of SQL queries that can be used with the custom query feature (note: cx_Oracle syntax does not require semicolons at the end):

SELECT * FROM product WHERE price > 5

SELECT * FROM customer

SELECT payment_method AS "Payment_Method", SUM(total_price) AS "Total Sales" FROM receipt GROUP BY payment_method

SELECT name, 'Works as a ' || position || ' for Shoppers Drug Mart' AS "Job Description" FROM employee

INSERT INTO product (product_id, category, product_name, price, shelf_quantity) VALUES (1, 'Fruit', 'Apple', 0.99, 10)
