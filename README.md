# MIS 311 - Sales Data Analysis Portfolio Project

## Project Overview

This repository presents my individual project for MIS 311 - Introduction to Business Analytics. In this project, I used Microsoft Excel to perform Exploratory Data Analysis on a sales dataset.

The purpose of this project is not only to calculate total sales, but also to understand what the data means in a business context. I focused on cleaning the dataset, calculating descriptive statistics, creating PivotTables and charts, and explaining two main insights from the data.

The analysis follows four main parts:

1. Data Overview  
2. Data Cleaning  
3. Descriptive Statistics  
4. Insights  

Through this project, I wanted to answer two practical business questions:

1. Which product categories contribute the most to total revenue?
2. Which customer type creates stronger sales performance?

These questions are important because they can help a business improve inventory planning, promotion strategy, and customer relationship management.

---

## 1. Data Overview

The dataset contains sales transaction records from different branches, cities, customer types, products, and product categories. It represents a realistic business situation where a company needs to understand its sales performance based on transaction data.

The original dataset contains **253 sales transaction records** and **8 main columns**:

| Column | Description |
|---|---|
| sale_id | Unique ID for each sales transaction |
| branch | The branch where the sale was made |
| city | The city where the transaction occurred |
| customer_type | Type of customer, such as Member, Normal, or Unknown |
| product_name | Name of the product sold |
| product_category | Category of the product |
| quantity | Number of units sold |
| total_price | Total value of the sales transaction |

The dataset includes both categorical and numerical variables.

Categorical variables such as `city`, `customer_type`, and `product_category` are useful for comparing different business segments. Numerical variables such as `quantity` and `total_price` are used to measure sales volume and revenue performance.

I selected this dataset because it allows me to connect data analysis with real business decisions. For example, if a business knows which product categories and customer groups perform better, it can make better decisions about inventory, promotion, and customer loyalty programs.

---

## 2. Data Cleaning

Before doing the analysis, I cleaned the dataset carefully. This step is important because incorrect or duplicated data can lead to misleading results. If duplicated transactions are not removed, total revenue will be overstated and the business may think its sales performance is stronger than it actually is.

### Missing Values

I first checked the dataset for missing values by using Excel filters. The result showed that there were **no blank missing values** in the main columns.

| Column | Missing Values |
|---|---:|
| sale_id | 0 |
| branch | 0 |
| city | 0 |
| customer_type | 0 |
| product_name | 0 |
| product_category | 0 |
| quantity | 0 |
| total_price | 0 |

Although there were no blank cells, I found some records marked as **Unknown**. I treated these values carefully because "Unknown" is not a blank value, but it still shows incomplete classification in the dataset.

### Customer Type

For `customer_type`, there were **3 records** marked as **Unknown**.

I decided not to delete these records because they still contained valid transaction information such as city, product name, quantity, and total price. If I removed them, the dataset would lose real sales transactions.

Instead, I kept **Unknown** as a separate customer type. This is a more reasonable decision because it keeps the sales value in the dataset while still showing that some customer information was not properly recorded.

In a real business situation, this could happen when the cashier forgets to select the customer type or when the system does not capture customer information correctly.

### Product Category

For `product_category`, there were **6 records** marked as **Unknown**.

I also kept these records as a separate category instead of deleting them because the transactions still had valid revenue and quantity values. Removing them would reduce the accuracy of total sales.

However, I did not combine Unknown with any other product category because there was not enough evidence to classify those products correctly. In business analytics, it is better to clearly show unknown data than to guess and create inaccurate results.

### Quantity

For `quantity`, I checked whether there were missing or unreasonable values. There were no blank values in this column.

I also calculated the median quantity in Excel:

```excel
=MEDIAN(G:G)
