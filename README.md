# DATA-ANALYST-INTERNSHIP-Elevate-Labs-Task-14

# Retail E-Commerce ETL Pipeline (Olist Dataset)

## Objectives
- Load raw e-commerce datasets from CSV files
- Perform data cleaning and preprocessing
- Standardize column names and datatypes
- Create derived business metrics
- Split processed data into logical entities
- Export outputs as CSV files
- Load results into a SQLite database
- Validate row counts to ensure data integrity

---

## Dataset Source
**Brazilian Olist Public E-Commerce Dataset (Kaggle)**

Files used:
- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_products_dataset.csv`
- `olist_customers_dataset.csv`

---


---

## ETL Workflow

### 1. Extract
Raw CSV datasets were loaded using Pandas:
- Orders dataset
- Order items dataset
- Products dataset
- Customers dataset

A folder structure was created to separate raw, processed, and output layers.

---

### 2. Transform

#### Data Cleaning
- Removed duplicate records
- Handled missing values
- Standardized column names to lowercase
- Converted timestamp columns into datetime format

#### Feature Engineering
Derived columns created:
- **margin** = price − freight_value
- **high_value_flag** → identifies high-value transactions

These transformations simulate real retail analytics logic.

---

### 3. Data Modeling & Splitting
The processed dataset was split into separate logical outputs:

**customers.csv**
- customer_id
- customer_unique_id
- customer_city
- customer_state

**products.csv**
- product_id
- product_category_name

**orders.csv**
- order_id
- product_id
- price
- freight_value
- margin
- high_value_flag

This structure resembles a simplified analytical data model.

---

### 4. Load
Final datasets were exported to CSV and loaded into a SQLite database.

SQLite tables created:
- customers
- products
- orders

---

### 5. Validation
Row counts were validated before and after transformation to ensure data consistency.

Validation checks included:
- Original vs processed row counts
- Output dataset record counts
- Data integrity after merges

---

## Tech Stack
- Python
- Pandas
- SQLite3
- Jupyter Notebook

---

## Key Learnings
- Building an end-to-end ETL workflow
- Data cleaning and preprocessing best practices
- Feature engineering with Pandas
- Structuring datasets for analytics
- Exporting and loading data into SQLite
- Maintaining reproducible pipelines

---

## Conclusion
This project demonstrates a professional ETL pipeline using real-world retail data.  
It highlights the ability to extract raw datasets, transform them into structured analytical outputs, and load them into a database for further analysis — reflecting common practices used in modern data engineering and analytics workflows.


## 🏗️ Project Structure
