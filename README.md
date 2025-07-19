# 📊 Sales Insights Dashboard (Tableau + MySQL)

An end-to-end Business Intelligence project that integrates a MySQL database with **Tableau** to create a powerful and interactive **Sales Insights Dashboard**. This solution enables real-time business performance analysis across customer types, time periods, and product lines.

---

## 📁 Project Files

- `Data Preprocessing_v2025.1.twb`: Tableau Workbook file with dashboards and data visuals.
- `database.sql`: SQL script to create and populate `sales` database tables.

---

## 🧱 Database Design

This project is backed by a normalized relational database containing:

- **customers**: Details about customer types (Brick & Mortar, E-Commerce)
- **date**: Date dimension table with various formats for reporting
- *(Optional additional tables like sales or transactions assumed to exist in Tableau joins)*

Sample Tables:
```sql
CREATE TABLE customers (
  customer_code VARCHAR(45) PRIMARY KEY,
  custmer_name VARCHAR(45),
  customer_type VARCHAR(45)
);

CREATE TABLE date (
  date DATE PRIMARY KEY,
  cy_date DATE,
  year INT,
  month_name VARCHAR(45),
  date_yy_mmm VARCHAR(45)
);
```
---

## 📊 Key Dashboard Features

- Revenue Trends Over Time using **Line Charts**
- Sales Quantity Trends using **Line Charts**
- Revenue by Markets using **Bar Charts**
- Sales Quantity by Markets using **Bar Charts**
- Top 5 Customers by Revenue using **Horizontal Bar Charts**
- Top 5 Products by Revenue using **Horizontal Bar Charts**
- Monthly and Yearly Revenue Comparison using **Line and Bar Charts**
- Time-based Filtering by **Year** and **Month**

---

## 🛠️ Tools Used

- Tableau Desktop for interactive dashboards  
- MySQL for database backend  
- SQL Workbench / CLI to run database schema (`database.sql`)

---

## 🚀 How to Run

1. Clone or download this repository.
2. Import the SQL script into your MySQL server:
   ```bash
   mysql -u root -p < database.sql
3. Open `Data Preprocessing_v2025.1.twb` in Tableau Desktop.  
4. Connect to the `sales` MySQL database when prompted.  
5. Refresh all Tableau data sources.  
6. Use filters to explore data by date, customer type, and other attributes.

---

## 📌 Use Case

- Analyze time-based sales and revenue performance  
- Compare customer behavior across Brick & Mortar vs E-Commerce  
- Identify high-performing regions and product categories  
- Support data-driven strategic decision-making  
- Enable interactive, filterable business reporting

