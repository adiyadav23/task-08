# Task 7: Basic Sales Summary using Python and SQLite
## Objective
The goal of this task is to use SQL inside Python to:
- Extract simple sales summaries (total quantity sold, total revenue per product)
- Visualize the results using a bar chart

## Tools Used
- Python
- SQLite (via sqlite3)
- pandas
- matplotlib
 Google Colab

## Dataset
A simple SQLite database named sales_data.db was created with a single table sales containing the following columns:
- product (TEXT)
- quantity (INTEGER)
- price (REAL)

### Sample Data:
```sql
('Product A', 10, 5.0)
('Product B', 7, 7.5)
('Product A', 3, 5.0)
('Product C', 5, 6.0)
('Product B', 4, 7.5)
('Product C', 2, 6.0)
SQL Query Used
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
Python Code Summary
	•	Connects to SQLite database using sqlite3
	•	Runs SQL query and loads result into a DataFrame using pandas
	•	Displays the result with print()
	•	Creates a bar chart using matplotlib

Output

A printed table of total quantity and revenue per product, and a bar chart titled “Revenue by Product”.

How to Run
	1.	Clone the repo or open the notebook in Google Colab.
	2.	Run the Python code to create the database, execute SQL, and visualize the results.

Learning Outcomes
	•	Connecting Python to SQLite
	•	Executing SQL queries inside Python
	•	Using pandas for data analysis
	•	Visualizing SQL results with matplotlib