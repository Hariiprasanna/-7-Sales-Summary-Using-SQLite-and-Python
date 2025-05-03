#  Basic Sales Summary Using SQLite and Python

## Objective

This project demonstrates how to:
- Create a **SQLite database** with sales data
- Run **SQL queries inside Python**
- Display **total quantity sold** and **total revenue**
- Visualize results using a **bar chart**

All done using Python’s built-in `sqlite3`, `pandas`, and `matplotlib` libraries.

##  Dataset

A small synthetic sales dataset (`sales_data.db`) is created with a single table:

**Table: `sales`**

| Column    | Type    | Description                   |
|-----------|---------|-------------------------------|
| sale_id   | INTEGER | Unique ID for each sale       |
| product   | TEXT    | Product name (e.g., Laptop)   |
| quantity  | INTEGER | Units sold                    |
| price     | REAL    | Price per unit                |

The dataset includes **30 random entries** across 5 product types.

## Tools Used

- **Python 3**
- **SQLite** (via `sqlite3` module)
- **Pandas** for data handling
- **Matplotlib** for visualization
- **Jupyter Notebook** or `.py` script

## SQL Query Used

```sql
SELECT 
    product,
    SUM(quantity) AS total_qty,
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;


 ## Output
Printed summary table of quantity sold and revenue per product
Bar chart saved as sales_chart.png


## Repository Contents
File	Description
sales_data.db	SQLite database containing sales table
task7_sales_summary.py	Python script used to run the analysis
sales_chart.png	Bar chart showing revenue by product
README.md	Project documentation (this file)
'''
