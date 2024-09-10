---
title: 'ML4LM— Cleaning the Data'
date: 2023-11-23
permalink: /posts/2023/11/blog-post-4/
tags:
  - Machine Learning
  - Data Cleaning
---

ML4LM- Cleaning the Data
Cleaning data for Machine learning is like preparing for a road trip where your model is the driver, and your data is the map. However, the map is a mishmash of routes, some as straightforward as a highway, while others resemble a convoluted maze that even a GPS would find confusing.
Missing Data:

In the realm of data, our info comes from diverse channels, creating a jigsaw puzzle. Sometimes, pieces need to be included, disrupting the flow of our machine-learning models. Our job is to decide: Do we fill those gaps or bid farewell to incomplete data records? The goal is to ensure our models churn out insights seamlessly.
For example, in an employee performance dataset, the "Years of Experience" column has missing values, potentially due to administrative errors or new hires. To address this, you can fill the gaps with the mean or median, or choose to exclude records with missing data based on the specific use case and dataset characteristics.
import pandas as pd

# Replace missing values in 'Years of Experience' with the median
df['Years of Experience'].fillna(df['Years of Experience'].median(), inplace=True)
2. Outliers and Noise:
Think of outliers in data cleaning like the one person wearing a flashy costume at a black-tie event - they stand out a lot! These are the oddballs that stray from the usual crowd, making them rebels in our dataset.
For example, In a dataset of monthly sales figures for a retail store, imagine the typical daily sales range is $1,000 to $5,000. However, there's an outlier where sales for a single day spike to $50,000. This extreme deviation could significantly impact average sales calculations and needs careful handling during data cleaning to ensure accurate insights into the store's usual performance.
Well, there are various techniques to identify outliers in a dataset. Some commonly used methods are Visualizing using box plots, IQR (Interquartile Range), Isolation Forest, Z-score and others.
Let's talk about IQR. It is a measure that helps us understand how spread out our data is. Imagine you have a list of numbers representing, let's say, daily sales. If you arrange these numbers in order, the IQR is the range that covers the middle portion of your data, between the 25th and 75th percentiles. In simpler terms, it gives you an idea of where most of your data lies and helps identify values that might be too far from the typical range.
# Remove outliers in 'Daily Sales' using the Interquartile Range (IQR)
import numpy as np

# Calculate the IQR
Q1 = df['Daily Sales'].quantile(0.25)
Q3 = df['Daily Sales'].quantile(0.75)
IQR = Q3 - Q1

# Set the threshold for outlier detection (e.g., 1.5 times IQR)
threshold = 1.5 * IQR

# Remove outliers
df_cleaned_sales = df[(df['Daily Sales'] >= (Q1 - threshold)) & (df['Daily Sales'] <= (Q3 + threshold))]
3. Inconsistent Data:
Inconsistent data occurs when information in a dataset lacks uniformity. For example, in a product price dataset, having values in both dollars and euros creates inconsistency. To ensure clarity and reliability, it's essential to standardize all prices into a single currency.
# Convert all prices to dollars
df['Price'] = df.apply(lambda row: row['Price'] * 1.18 if row['Currency'] == 'Euro' else row['Price'], axis=1)
4. Duplicate Data
In the database of online orders, duplicate entries arise when the same order is inadvertently recorded more than once, often due to glitches in the order processing system. These duplicates can lead to inaccuracies in analytics and reporting, emphasizing the importance of identifying and rectifying such redundancy to maintain the integrity of the data.
# Remove duplicate rows based on the 'Order ID' column
df.drop_duplicates(subset='Order ID', inplace=True)
5. Data Encoding
Data encoding in data cleaning is crucial, especially when dealing with categorical information like payment methods in an e-commerce dataset ('Credit Card' and 'PayPal'). This conversion to numerical representations, often done through techniques like one-hot encoding, is necessary because machine learning models inherently understand and process numerical values. This step ensures seamless integration of categorical data into the training process, allowing models to glean insights and make predictions effectively. Or a more easy example could be a Gender column with Male and Female as values.
# Map categorical values to numerical codes
payment_method_mapping = {'Credit Card': 0, 'PayPal': 1}
df['Payment Method'] = df['Payment Method'].map(payment_method_mapping)
Thanks for reading! We will continue enhancing this and explore more exciting aspects. Stay tuned for some interesting insights!