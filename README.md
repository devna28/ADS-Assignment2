Smartphone Dataset Cleaning & Recommendation System

A Jupyter Notebook project demonstrating real-world data cleaning and a simple product recommendation system using a smartphone dataset (smartphones.csv). Learn how to handle messy data and create a searchable, clean dataset for analysis.

 Features

Data Cleaning & Preprocessing

Handle missing values, duplicates, and inconsistent formats.

Convert textual data like "8 GB" or "5000 mAh" to numeric types.

Correct data types and ensure consistency for analysis.

Exploratory Data Analysis

Dataset overview: shape, columns, missing values.

Descriptive statistics for numerical features.

Optional visualization using Matplotlib/Seaborn.

Recommendation System

Simple text-based search function to find smartphones by model or keyword.

Supports case-insensitive search and returns relevant product details.

 Workflow

Load the Dataset

Load smartphones.csv and preview data.

Explore the Dataset

Check column types, missing values, and top records.

Clean the Data

Handle missing values for price, rating, camera, OS, and expandable storage.

Remove duplicates and clean text columns.

Extract numeric values for RAM, battery, display, etc.

Export Cleaned Data

Save cleaned dataset as smartphones_cleaned.csv.

Use Recommendation Function

Search products by keyword using the recommend_products() function.

Recommendation Function
def recommend_products(keyword, df, column="model"):
    results = df[df[column].str.contains(keyword, case=False, na=False)]
    return results


Example:

recommend_products("Samsung", df)


Sample Output:

model	price	rating	ram_gb	battery_mah	display_inches	os
Samsung Galaxy S21	69999.0	4.3	8	4000	6.2	Android
Samsung Galaxy A52	25999.0	4.1	6	4500	6.5	Android Files

smartphones.csv — Raw input dataset

smartphones_cleaned.csv — Cleaned and processed dataset

smartphone.ipynb — Jupyter Notebook with code, explanations, and recommendations
