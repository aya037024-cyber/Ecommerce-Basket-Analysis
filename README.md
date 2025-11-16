# Ecommerce Basket Analysis

## Overview
This project analyzes the shopping basket data of an e-commerce store. The main goal is to understand customer purchasing behavior, identify top products, explore basket sizes, and visualize daily sales trends. The analysis helps in generating actionable insights for marketing and inventory planning.

---

## Datasets

### 1) basket_details.csv
Contains information about each shopping basket:

- `customer_id` – Unique ID of the customer  
- `product_id` – Unique ID of the product purchased  
- `basket_date` – Date of the basket  
- `basket_count` – Number of products in the basket  

### 2) customer_details.csv
Contains information about customers:

- `customer_id` – Unique ID of the customer  
- `sex` – Gender of the customer  
- `customer_age` – Age of the customer  
- `tenure` – Number of days the customer has been active  

---

## Data Cleaning and Preparation
- Converted `basket_date` to datetime format for time-based analysis  
- Merged `basket_details` and `customer_details` on `customer_id` (most customers missing in customer_details, so main analysis focuses on basket data)  
- Added derived columns:
  - `Year` and `Month` extracted from `basket_date`  
  - `Basket_Size` categorized as Small (1–2 items), Medium (3–5 items), Large (6+ items)  

---

## Exploratory Data Analysis (EDA)

### Basket Size Distribution
- Small: **13,323 baskets**  
- Medium: **1,623 baskets**  
- Large: **54 baskets**

> **Insight:** Most customers purchase only 1–2 items per basket, indicating low-value and quick purchases.

### Top Products
| Product ID | Purchase Count |
|------------|----------------|
| 43524799   | 32             |
| 31516269   | 25             |
| 39833031   | 24             |
| 46130148   | 17             |
| 40276011   | 12             |

> **Insight:** No single product dominates sales; the most popular product was bought only 32 times, reflecting a wide product variety.

### Daily Basket Trend
- Line chart shows the number of baskets per day over the dataset period.  
- Identifies peak sales days and seasonal trends.

---

## Visualizations
- **Distribution of Basket Sizes** – Bar chart  
- **Top 10 Products** – Bar chart  
- **Daily Basket Count** – Line chart  

> Charts are included in the `images/` folder.

---

## Tools and Libraries
- Python 3.x  
- Pandas  
- Matplotlib   
- Jupyter Notebook  
- VS Code  

