# Database-Development-for-Shoppers-Drug-Marts
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

Once installed, start CS VPN connection and run main.py and login with your proper cs credentials to access the DB.

You can begin by dropping all tables to start the DB from fresh, followed by selecting "Create all tables" to create tables in the DB.

"Populate all tables" will fill the tables with dummy data. 

"Query All Tables" will run a couple advanced queries and display the results of the queries.

"Show all Tables" will show tables currently in the DB.

"Run Custom Query" allows you to input your own syntactically correct sql query in the text field and run it once clicked.

"Drop all Tables" removes all tables from the DB.

"Exit" closes the program

Below are some sample queries you can run using the custom query input (note: cx_oracle syntax does not require semicolons at the end of statements):

SELECT * FROM product WHERE price > 5 

SELECT * FROM customer

SELECT payment_method AS "Payment_Method", SUM(total_price) AS "Total Sales" FROM receipt GROUP BY payment_method

SELECT name, 'Works as a ' || position || ' for Shoppers Drug Mart' AS "Job Description" FROM employee

INSERT INTO product (product_id, category, product_name, price, shelf_quantity) VALUES (1, 'Fruit', 'Apple', 0.99, 10)
