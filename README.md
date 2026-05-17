# MIS 311 - Sales Data Analysis Project

## Project Overview

This project is my individual assignment for MIS 311 - Introduction to Business Analytics. I used Microsoft Excel to perform Exploratory Data Analysis on a sales dataset.

The goal of this project is to clean the dataset, calculate descriptive statistics, create PivotTables and charts, and explain key business insights from the sales data.

The analysis focuses on two main questions:

1. Which product categories contribute the most to total revenue?
2. Which customer type creates stronger sales performance?

## Dataset Overview

The dataset contains sales transaction records from different branches, cities, customer types, products, and product categories.

The original dataset has **253 records** and **8 columns**:

- sale_id
- branch
- city
- customer_type
- product_name
- product_category
- quantity
- total_price

The dataset includes both categorical variables, such as city and customer type, and numerical variables, such as quantity and total price.

## Data Cleaning

Before analysis, I checked the dataset for missing values, unknown values, and duplicate rows.

There were no blank missing values in the main columns. However, some records were marked as **Unknown** in `customer_type` and `product_category`. I kept these records as separate categories because they still contained valid sales information.

I also found and removed **3 exact duplicate rows**. After cleaning, the dataset had **250 records**.

| Cleaning Result | Value |
|---|---:|
| Original records | 253 |
| Duplicate rows removed | 3 |
| Final records | 250 |
| Revenue before cleaning | 31,312.78 |
| Revenue after cleaning | 31,046.28 |

This step is important because duplicated transactions can overstate total revenue and lead to inaccurate business conclusions.

## Descriptive Statistics

After cleaning the data, I calculated descriptive statistics for `quantity` and `total_price`.

| Statistic | Quantity | Total Price |
|---|---:|---:|
| Count | 250 | 250 |
| Sum | 2,654 | 31,046.28 |
| Mean | 10.62 | 124.19 |
| Median | 11.00 | 95.43 |
| Standard Deviation | 5.99 | 102.98 |

The average quantity per transaction is **10.62**, while the median quantity is **11**. This shows that a typical transaction contains around 10 to 11 units.

The average transaction value is **124.19**, while the median is **95.43**. This means some high-value transactions pull the average upward.

## Key Insights

### Insight 1: Revenue by Product Category

Fruits generated the highest total revenue, with **7,505.08**, accounting for **24.17%** of total revenue. This means Fruits is an important category for overall sales performance.

However, Stationery had the highest average revenue per transaction, at **142.16**. This shows that total revenue and average transaction value can tell different business stories.

A practical decision would be to maintain strong inventory for Fruits while using Stationery and Beverages for bundle promotions or cross-selling.

### Insight 2: Revenue by Customer Type

Member customers generated **17,855.87**, which accounts for **57.51%** of total revenue. Normal customers generated **13,106.73**, equal to **42.22%** of total revenue.

Member customers also had a higher average transaction value, spending **136.30** per transaction compared with **112.99** for Normal customers.

This suggests that the membership group is valuable to the business. The company should maintain current members and encourage Normal customers to become members through reward points, discounts, or loyalty benefits.

## Tools Used

- Microsoft Excel
- Excel Filter
- Remove Duplicates
- Descriptive Statistics
- PivotTable
- Column Chart

## Repository Contents

| File / Folder | Description |
|---|---|
| `README.md` | Project summary |
| `data/` | Sales dataset |
| `charts/` | Excel charts |
| `report/` | Final assignment report |

## What I Learned

This project helped me understand that data cleaning is necessary before creating insights. I also learned that different measures can tell different stories. For example, Fruits leads in total revenue, but Stationery has the highest average transaction value, while Member customers show stronger spending behavior than Normal customers.
