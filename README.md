# Task-3-SQL-For-Data-Analysis

SQL Functions Used

🔧 Database & Table Creation
•	CREATE DATABASE
o	Creates a new database (TASK3SQLDATAANALYSIS).
•	USE
o	Selects the created database for subsequent operations.
•	CREATE TABLE
o	Defines two tables: orders_data and returns_data with specific data types.
________________________________________
📥 Data Insertion
•	INSERT INTO
o	Inserts bulk data into orders_data and returns_data.
________________________________________
🔍 Basic Data Retrieval
•	SELECT
o	Retrieves all or specific columns.
o	Examples:
	SELECT * FROM orders_data;
	SELECT order_id, order_date, sales FROM orders_data;
•	SELECT TOP (n)
o	Retrieves the top n records.
o	Example: SELECT TOP 10 * FROM orders_data;
________________________________________
📌 Filtering Data
•	WHERE
o	Filters rows based on condition.
o	Examples:
	WHERE city = 'Henderson'
	WHERE profit > 100
•	AND / OR
o	Combines multiple conditions.
o	Examples:
	WHERE category = 'Furniture' AND profit > 100
	WHERE city = 'Los Angeles' OR order_date > '2020-11-08'
________________________________________
📊 Sorting Data
•	ORDER BY
o	Sorts results by one or more columns.
o	Examples:
	ORDER BY order_date
	ORDER BY order_date DESC, profit DESC
________________________________________
📐 Aggregate Functions
•	SUM()
o	Calculates total.
o	Example: SUM(quantity) AS Sum_of_Sales
•	MAX()
o	Retrieves the maximum value.
o	Example: SELECT MAX(SALES) AS TOTAL_SALES
________________________________________
📦 Grouping Data
•	GROUP BY
o	Aggregates data by category.
o	Example:
sql
CopyEdit
SELECT category, SUM(sales), SUM(profit)
FROM orders_data
GROUP BY category;
•	HAVING
o	Filters results from GROUP BY.
o	Example:
sql
CopyEdit
SELECT city, SUM(sales) AS city_sales
FROM orders_data
WHERE region = 'West'
GROUP BY city
HAVING SUM(sales) > 500;
________________________________________
🔗 Joins
•	INNER JOIN
o	Combines rows with matching order_id.
•	LEFT JOIN, RIGHT JOIN
o	Includes unmatched rows from one table.
________________________________________
🔍 Indexing
•	CREATE INDEX
o	Speeds up retrieval on returns_data(order_id).
________________________________________
🪟 Views
•	CREATE VIEW
o	Defines a virtual table (City) showing customers in Henderson.
________________________________________
✅ Summary of Functions Used
Function / Keyword	Description
CREATE DATABASE	Creates a new database
USE	Selects database context
CREATE TABLE	Defines table schema
INSERT INTO	Adds data records
SELECT, TOP	Retrieves data
WHERE, AND, OR	Filters records
ORDER BY	Sorts records
SUM(), MAX()	Aggregate computations
GROUP BY, HAVING	Groups data and filters aggregated rows
JOIN, LEFT/RIGHT JOIN	Combines related data across tables
CREATE INDEX	Optimizes search queries
CREATE VIEW	Creates a virtual table

