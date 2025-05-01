# 🛒 Task 7 - Basic Sales Summary using SQLite & Python

## 🎯 Objective

To analyze sales data using a simple SQLite database and visualize basic metrics like **total quantity sold** and **total revenue** using **Python**, **SQL**, **Pandas**, and **Matplotlib**.

---

## 🧰 Tools & Libraries Used

- **Python**
- **SQLite3** (built-in Python module)
- **Pandas** (for data analysis)
- **Matplotlib** (for data visualization)
- **Jupyter Notebook**

---

## 🗃️ Dataset Structure

A sample dataset with sales records is stored in a SQLite database file `sales_data.db`.  
The database contains one table: `sales`.

### `sales` Table Columns:
- `id` (Primary Key, auto-increment)
- `product` (Text)
- `quantity` (Integer)
- `price` (Real)

---

## 🧮 SQL Query Used

```sql
SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
