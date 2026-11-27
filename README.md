## Project Overview

This project is the result of my work during a Boston Consulting Group data challenge organized in February 2026. 
The goal was to create a machine learning model that predicts if a customer will purchase again, starting the 1st of October 2012.
It was the opportunity to manipulate data and to build a classification model.

---

## Objectives

* Build meaningful customer-level features from raw transaction data
* Define and analyze high-potential customers
* Use clustering to uncover behavioral patterns

---

## Data

The raw data comes from the BCG data challenge and is not included in this repository. The notebook expects two CSV files in the same folder (`DATA_DIR = "./"`): `transactions_data.csv` and `product_data.csv`. This section describes them so the notebook can be read without the files.

### 1. `transactions_data.csv`

One row per product line in an order (42,820 rows, 6 columns, no missing values).

| Column | Type | Description |
|---|---|---|
| `transaction_id` | int | ID of an order. Products bought together share the same ID (2,461 distinct orders). |
| `product_id` | int | ID of the product bought (2,993 distinct products). |
| `purchased_quantity` | int | Number of units bought. Negative values (~940 rows) correspond to returns or cancellations. |
| `transaction_date` | string | Date and time of the order, formatted `dd/mm/yyyy HH:MM` (day first). Ranges from 5 January 2012 to 12 January 2013. |
| `unit_product_price` | float | Price of one unit of the product. |
| `customer_id` | int | ID of the customer (487 distinct customers). |

### 2. `product_data.csv`

One row per product (2,993 rows, 2 columns, `product_id` is unique).

| Column | Type | Description |
|---|---|---|
| `product_id` | int | Product ID, used to join with `transactions_data.csv`. |
| `color` | string | Color of the product: black, white, blue, red, green or yellow. Missing for 48 products. |

---

## Methodology

### 1. Data Preparation

* Loading data
* Filtering data into training period

### 2. Feature Engineering

* Construction of customer-level features using aggregation
* Definition of the Target Variable, being returning customers

### 3. Generalized Linear Model

* Logistic Regression Model
* Evaluation of the model's performance
* Comparison with a Random Forest

### 4. High Potential Customer Detection

* Implementation of a K-means clustering method
* Evaluation of the model's performance

---

## Technologies Used

* Python
* pandas
* numpy
* scikit-learn
* matplotlib
