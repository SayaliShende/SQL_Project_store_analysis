# NEW_STORE_ANALYSIS_FOR_RETAIL_GIANT_XYZltd.
The project provides an understanding of relational database management and demonstrate the practical application of SQL in addressing real-world queries related to monitoring and analyzing the sales of newly established mini stores for "XYZ Ltd."


### Project Objective
The aim of this project is to provide an understanding of relational database management and demonstrate the practical application of SQL in addressing real-world queries related to monitoring and analyzing the sales of newly established mini stores for "XYZ Ltd."

### Business Problem
"XYZ Ltd." is a retail giant operating grocery stores, e-commerce, and departmental stores. The company has recently set up mini stores focusing on groceries, fresh produce, dairy, and poultry items.

### Objective:
The company wants to develop a database to track and monitor the sales of these new mini stores to determine their profitability and inform the management if it is worth continuing to open such stores.

As the designated Database Administrator, your role will be to design, implement, and manage the transaction database for these mini stores, providing insights into their sales performance.
### Project Scope and Features
#### 1.	Database Design:
o	Design a relational database schema to capture key entities and relationships related to the sales of mini stores.
o	Key entities include: Products, Stores, Inventory, Sales, and Transactions.
#### 2.	Sales Monitoring:
o	Record sales transactions for mini stores.
o	Generate reports on total sales, top-selling products, and sales trends over time.
#### 3.	Profitability Analysis:
o	Calculate the profitability of each mini store.
o	Compare sales performance across different locations.

### Database Schema: 
### Entities and Relationships:
•	Products: product_id, product_name, category, price

•	Stores: store_id, store_name, location

•	Inventory: inventory_id, store_id, product_id, stock_level, reorder_level

•	Sales: sale_id, store_id, product_id, sale_date, quantity_sold, total_amount

•	Transactions: transaction_id, sale_id, payment_method, transaction_date


#### Steps to Implement the Project

1.	Requirements Gathering:
      Stakeholders analysis to understand their data needs and reporting requirements.
      Identify key metrics and performance indicators for sales monitoring and profitability analysis.
2.    Database Design:
      Creating an Entity-Relationship Diagram (ERD) to model the database structure.
      Define tables, primary keys, foreign keys, and relationships.
3.	Database Implementation:
      Using SQL to create the database schema based on the ERD.
      Populate the database with sample data for testing.
4.    Data Integration:
      Developing scripts to import data from various sources into the database.
      Ensuring data consistency and integrity.
5.	Query Development:
      Writing SQL queries to extract and analyze data.
      Optimizing queries for performance.
6.	Reporting and Visualization:
      Using tools like SQL Server Reporting Services (SSRS), Tableau, or Power BI to create reports and dashboards.
      Providing stakeholders with access to real-time data and insights


### Business Understanding
Business Context: "XYZ Ltd." is a retail giant operating in various segments, including grocery stores, e-commerce, and departmental stores. The company has recently expanded its operations by setting up mini stores that focus specifically on groceries, fresh produce, dairy, and poultry items. These mini stores are intended to cater to local neighborhoods, providing convenient access to essential items.
Business Objective: The primary goal is to develop a robust database system to track and monitor the sales performance of these mini stores. This system will help the management analyze whether the new mini stores are profitable and determine if it is worth continuing and expanding this business model.

### Business Rules
1.	Product Management:
	 -Each product must have a unique identifier (product_id).
	 -Products are categorized into distinct categories (e.g., groceries, fresh produce, dairy, poultry).
	 -Product prices are stored and can be updated as needed.
2.	Store Management:
	 -Each mini store must have a unique identifier (store_id).
	 -Stores are identified by their name and location.
3.	Inventory Management:
	 -Inventory levels must be tracked for each product at each store.
	 -Each inventory entry must have a reorder level, which triggers restocking when the stock falls below this level.
	 -Inventory levels are updated with each sale transaction.
4.	Sales Transactions:
	 -Each sale transaction must have a unique identifier (sale_id).
	 -Sales must be recorded with the date, store_id, product_id, quantity_sold, and total_amount.
	 -Sales transactions must update the inventory levels accordingly.
5.	Transactions:
	 -Each transaction must have a unique identifier (transaction_id).
	 -Transactions record the payment method and the date of the transaction.
	 -Each transaction is linked to a sale.
6.	Reporting and Analysis:
	 -The system must be able to generate reports on total sales by store, top-selling products, and sales trends over time.
	 -Profitability reports must compare sales revenue against product costs to determine profit margins.
	 -Reports must be generated for different time periods (daily, weekly, monthly).

### Entity-Relationship Diagram (ERD) Analysis
#### Entities and Attributes:
1.	Products:
	product_id (Primary Key),
	product_name,
	category,
	price
2.	Stores:
	store_id (Primary Key),
	store_name,
	location
3.	Inventory:
	inventory_id (Primary Key),
	store_id (Foreign Key),
	product_id (Foreign Key),
	stock_level,
	reorder_level
4.	Sales:
	sale_id (Primary Key),
	store_id (Foreign Key),
	product_id (Foreign Key),
	sale_date,
	quantity_sold,
	total_amount
5.	Transactions:
	transaction_id (Primary Key),
	sale_id (Foreign Key),
	payment_method,
	transaction_date

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/ERD/SQL%20ERD%20PROJECT%20-%20Page%202.png" alt="Entity Relationship Diagram" width="700" height="500">

### ERD Relationships:
#### 1.	Store to Sales (One-to-Many Relationship): 
In this relationship, a single store can have many sales transactions, demonstrating a one-to-many relationship. This means that each store, such as Mini Store A, can handle multiple sales transactions over time. Each sale is uniquely associated with one store, ensuring that the sales data can be traced back to the specific location where the sale occurred. This relationship allows the company to analyze sales performance by store, monitor store-level sales trends, and make informed decisions about store operations and strategies.
#### 2. Product to Sales (One-to-Many Relationship)
This relationship illustrates that a single product can appear in multiple sales transactions, highlighting another one-to-many relationship. For example, a product like 'Milk' can be sold multiple times across various transactions in different stores. Each sale record contains details about the product sold, making it possible to track the sales volume and revenue generated by each product. This relationship is crucial for inventory management, sales forecasting, and understanding product popularity, helping the company optimize product availability and pricing strategies.
#### 3. Sale to Transaction (One-to-One Relationship)
Here, the relationship between a sale and a transaction is one-to-one, meaning each sale transaction is linked to a single transaction record. This ensures that every sale has an associated transaction that includes payment details and the transaction date. For instance, a sale of 'Milk' on June 1 will have a corresponding transaction record detailing the payment method used and the exact date of the transaction. This relationship is essential for accurate financial tracking, auditing, and ensuring that all sales are properly recorded and accounted for in the financial system.
#### 4. Store to Inventory (One-to-Many Relationship)
In this relationship, a single store can have multiple inventory records, each representing different products, forming a one-to-many relationship. Each store, such as Mini Store A, maintains inventory records for various products like 'Milk', 'Eggs', 'Apples', etc. These records include information about stock levels and reorder points, enabling the store to manage its inventory effectively. This relationship is key to ensuring that stores are adequately stocked, preventing stockouts, and optimizing the replenishment process to meet customer demand efficiently.
#### 5. Product to Inventory (One-to-Many Relationship)
This relationship indicates that a single product can be part of the inventory in multiple stores, again forming a one-to-many relationship. For instance, the product 'Milk' can be stocked in Mini Store A, Mini Store B, and Mini Store C. Each inventory record is tied to a specific product and a specific store, allowing the company to track where each product is available and in what quantities. This relationship is vital for maintaining optimal inventory levels across all stores, ensuring that products are available where needed, and supporting decisions about product distribution and stock management across the mini-store network.

### Designing a Database schema using MySql

     # Creating a Database for XYZ ltd
          CREATE DATABASE sql_project


     # Create Products Table

        CREATE TABLE Products 
        (
        product_id INT PRIMARY KEY,
        product_name VARCHAR(255),
        category VARCHAR(255),
        price DECIMAL(10, 2)
        );



    # Create Stores Table
        CREATE TABLE Stores 
        (
        store_id INT PRIMARY KEY,
        store_name VARCHAR(255),
        x
        );




    # Create Inventory Table
        CREATE TABLE Inventory (
        inventory_id INT PRIMARY KEY,
        store_id INT,
        product_id INT,
        stock_level INT,
        reorder_level INT,
        FOREIGN KEY (store_id) REFERENCES Stores(store_id),
        FOREIGN KEY (product_id) REFERENCES Products(product_id)
       );



    # Create Sales Table
       CREATE TABLE Sales (
       sale_id INT PRIMARY KEY,
       store_id INT,
       product_id INT,
       sale_date DATE,
       quantity_sold INT,
       total_amount DECIMAL(10, 2),
       FOREIGN KEY (store_id) REFERENCES Stores(store_id),
       FOREIGN KEY (product_id) REFERENCES Products(product_id)
       );



    # Create Transactions Table
        CREATE TABLE Transactions (
        transaction_id INT PRIMARY KEY,
        sale_id INT,
        payment_method VARCHAR(50),
        transaction_date DATE,
        FOREIGN KEY (sale_id) REFERENCES Sales(sale_id)
        );


### Solving the business problem by analysing few business related questions
### 1. Top selling products per store 

    SELECT p.product_id, p.product_name, s.store_id, SUM(s.quantity_sold) AS units_sold,
    ROW_NUMBER() OVER(PARTITION BY s.store_id ORDER BY SUM(s.quantity_sold) DESC) AS sale_rank
    FROM products p
    LEFT JOIN sales s ON p.product_id = s.product_id
    GROUP BY p.product_id, p.product_name, s.store_id
    ORDER BY s.store_id, sale_rank;

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/Query%201.png" alt="Entity Relationship Diagram" width="500" height="200">

### 2. Total sales by store
    SELECT Sales.store_id, Stores.store_name, SUM(Sales.total_amount) AS total_sales
    FROM Sales
    JOIN Stores ON Sales.store_id = Stores.store_id
    GROUP BY store_id, store_name
    ORDER BY total_sales DESC;

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/Query%202_.png" alt="Entity Relationship Diagram" width="600" height="200">

### 3. Sales Trends Over Time to understand the daily sales
    SELECT sale_date, SUM(total_amount) AS daily_sales
    FROM Sales
    GROUP BY sale_date
    ORDER BY sale_date;


<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/Query%203.png" alt="Entity Relationship Diagram" width="500" height="250">

### 4. Profit Analysis for the stores
    SELECT st.store_name, p.category,  sum(s.total_amount) - sum(p.price * s.quantity_sold) as profit
    FROM products p
    LEFT JOIN sales s on p.product_id = s.product_id
    LEFT JOIN stores st on st.store_id = s.store_id
    GROUP BY s.store_id, st.store_name
    ORDER BY profit DESC;

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/Query%204.png" alt="Entity Relationship Diagram" width="500" height="150">

### 5. Payment Method Analysis by store

    SELECT Stores.store_id, Transactions.payment_method, COUNT(*) AS transaction_count,
    SUM(sales.total_amount) AS total_sales,
    ROW_NUMBER() OVER (PARTITION BY stores.store_id ORDER BY SUM(sales.total_amount) DESC) AS transaction_rank
    FROM Transactions
    JOIN Sales ON Transactions.sale_id = Sales.sale_id
    JOIN Stores ON Sales.store_id = Stores.store_id
    GROUP BY Stores.store_id, Transactions.payment_method
    ORDER BY Stores.store_id, transaction_rank;

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/Query%205.png" alt="Entity Relationship Diagram" width="500" height="250">

### 6. Preferred Payment Method Analysis to understand the preferred payment methods
    SELECT payment_method, COUNT(*) AS transaction_count, SUM(total_amount) AS total_sales
    FROM Transactions
    JOIN Sales ON Transactions.sale_id = Sales.sale_id
    GROUP BY payment_method
    ORDER BY total_sales DESC;

<img src="https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/query_results/query%206.png" alt="Entity Relationship Diagram" width="500" height="180">

### Conclusion:
Relational Database Management Systems (RDBMS) are indispensable for managing modern databases, providing a structured and organized approach that ensures data integrity, security, and scalability. The use of SQL, a powerful query language designed for RDBMS, enables efficient data retrieval, manipulation, and analysis. This capability is crucial for businesses and applications that rely on precise and reliable data, particularly in sectors like finance and retail, where decision-making depends heavily on accurate information.

The analysis of XYZ Ltd.'s mini stores has revealed several key insights. Eggs and apples have emerged as the top-selling products across the stores, indicating a strong customer preference. The Neighbourhood A store stands out as the highest revenue generator, suggesting it has a significant customer base or purchasing power. Initial sales trends for May show positive growth, although a more extended period of data collection is necessary to draw substantial conclusions. Profitability analysis indicates that the stores are currently at break-even, and payment method analysis shows a balanced sales of credit cards, debit cards, and cash across stores with credit cards being the most frequently used transaction method.

### Recommendations:
1.Product Strategy: Given the high sales of eggs and apples, increase inventory levels for these items and consider targeted promotions to maximize revenue. This focus on popular products can help drive sales and customer satisfaction.

2.Store-Specific Investments: Invest more in marketing and customer experience enhancements at the Neighbourhood A store, which has demonstrated the highest sales performance. This store can serve as a model for other locations, potentially driving overall business growth.

3.Extended Sales Tracking: Continue tracking sales data over a longer period to confirm the positive growth trend observed in May. This will provide a more comprehensive understanding of sales patterns and help in making more informed decisions.

4.Profitability Enhancement: Conduct a detailed analysis to identify cost-saving opportunities and potential revenue increases to move beyond break-even. Consider optimizing inventory management, renegotiating supplier contracts, and enhancing promotional strategies to improve profitability.

5.Payment Method Optimization: Leverage the popularity of credit cards by offering incentives for their use, such as cashback or loyalty points. Ensure efficient processing for all payment methods to maintain high customer satisfaction and streamline transaction processes.

Implementing these recommendations will help XYZ Ltd. better understand customer preferences, optimize operations, and ultimately drive business growth and profitability. Continuous data analysis and informed decision-making will be key to the long-term success of the mini stores.

### References:
1. Retrieved from: Created in Lucidchart, www.lucidchart.com
2. Duong, E. (2023). Critical concepts in relational database — Data science journey. Medium. Retrieved June 10, 2024, from https://medium.com/@ethan.duong1120/8-critical-concepts-in-relational-database-80c74aa15e9c 
3. Retrieved from: Normalization, https://www.studytonight.com/dbms/database-normalization.php
4. Retrived from: MySql Documentation, https://dev.mysql.com/doc/workbench/en/




[https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/ERD/SQL%20ERD%20PROJECT%20-%20Page%202.png]: https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/ERD/SQL%20ERD%20PROJECT%20-%20Page%202.png
[https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/ERD/SQL%20ERD%20PROJECT%20-%20Page%202.png]: https://github.com/SayaliShende/SQL_Project_store_analysis/blob/main/ERD/SQL%20ERD%20PROJECT%20-%20Page%202.png