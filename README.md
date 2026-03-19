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

### 1. transaction_data.csv

Contains the products bought (product_id), the number of units bought (purchased_quantity), the price of the product per unit (unit_product_price),
the ID of a group of products bought together in a single order (transaction_id), the customer ID (customer_id), and the transaction date
(transaction_date).

### 1. product_data.csv

Contains the same products bought (product_id), and the color of the product if registered (color).

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
