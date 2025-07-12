# 🛒 Zepto E-commerce SQL Data Analyst Portfolio Project

This is a **complete, real-world SQL portfolio project** based on an e-commerce inventory dataset scraped from **Zepto**, one of India’s fastest-growing quick-commerce startups. The project simulates the real workflow of a data analyst — from messy raw data to actionable business insights.

---

## 🎯 Project Goal

To replicate how data analysts in e-commerce or retail use SQL for:
- Data cleaning and preparation
- Exploratory data analysis (EDA)
- Business-focused data queries
- Deriving insights around inventory, pricing, and revenue

---

## 👨‍💻 Ideal For

- 📊 Aspiring Data Analysts building a SQL portfolio  
- 💼 Candidates preparing for interviews in e-commerce, retail, or product analytics  
- 📚 Anyone learning SQL through real-world data  

---

## 📁 Dataset Overview

- The dataset is scraped from **Zepto’s official product listings** (sourced via Kaggle).
- Each row represents a **unique SKU (Stock Keeping Unit)**.
- Duplicate product names exist due to different package sizes, discounts, or categories — just like a real catalog.

### 📄 Key Columns

| Column                 | Description                                              |
|------------------------|----------------------------------------------------------|
| `sku_id`               | Unique ID for each product entry                         |
| `name`                 | Product name as listed on Zepto                          |
| `category`             | Product category (Fruits, Beverages, etc.)              |
| `mrp`                  | Maximum Retail Price (converted from paise to ₹)        |
| `discountPercent`      | Percentage discount applied                              |
| `discountedSellingPrice` | Final price after discount                           |
| `availableQuantity`    | Inventory units available                                |
| `weightInGms`          | Product weight in grams                                  |
| `outOfStock`           | Boolean flag for stock availability                      |
| `quantity`             | Units per package (mixed with grams for loose produce)  |

---

## 🛠️ Project Workflow

### 1. 🧱 Database & Table Creation

```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);


