# Electronics Sales Dataset README

This README provides an overview and usage instructions for the Electronics Sales dataset, which contains user ratings for various electronics items sold on Amazon. The dataset includes information such as the item ID, user ID, rating, timestamp, model attribute, category, brand, year, user attribute, and split.

## Dataset Information
- The dataset is available at [https://www.kaggle.com/datasets/edusanketdk/electronics](https://www.kaggle.com/datasets/edusanketdk/electronics).
- It consists of a CSV file named "electronics.csv".
- The dataset contains 1,292,954 rows and 10 columns.
- The columns include: `item_id`, `user_id`, `rating`, `timestamp`, `model_attr`, `category`, `brand`, `year`, `user_attr`, and `split`.

## Usage Instructions
To use the dataset, follow these steps:

1. Import the required libraries:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

2. Import the dataset:
```python
dataset = pd.read_csv('electronics.csv')
```

3. Explore the dataset:
- To view the first five rows of the dataset, use:
```python
dataset.head()
```

- To view the last five rows of the dataset, use:
```python
dataset.tail()
```

- To get the shape of the dataset (number of rows and columns), use:
```python
dataset.shape
```

- To get information about the dataset's columns and data types, use:
```python
dataset.info()
```

4. Data Preprocessing:
- Convert the `timestamp` column from object to Date & Time format:
```python
from datetime import datetime

dataset['timestamp'] = pd.to_datetime(dataset['timestamp'])
```

- Convert specific columns to their appropriate data types:
```python
dataset['brand'] = dataset['brand'].astype(str)
dataset['category'] = dataset['category'].astype(str)
dataset['timestamp'] = pd.to_datetime(dataset['timestamp'])
dataset['rating'] = dataset['rating'].astype(float)
dataset['user_id'] = dataset['user_id'].astype(str)
dataset['item_id'] = dataset['item_id'].astype(str)
```

5. Perform Data Analysis and Visualization:
The code provided in the README includes various examples of data analysis and visualization using the dataset. These examples cover topics such as the distribution of ratings, sales by year, sales by brand, sales by category, and more. Each code snippet is accompanied by a description and visualization output.

6. Conclusion:
Based on the analysis, the following conclusions can be made:
- The year 2015 had the best sales.
- The month of January had the highest sales.
- The brands Logitech and Sony sold the most.
- The category of Headphones had the highest sales.
- The brand Koolertron had the lowest sales.
- The category of Security and Surveillance had the lowest sales.

Please note that the provided code snippets are just examples, and you can further explore the dataset and perform additional analyses based on your specific requirements.

Feel free to modify and build upon the provided code to gain deeper insights into the electronics sales data at Amazon.
