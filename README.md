# Zomato-Data-Analysis-with-Python

## 📌 Disclaimer
This is a Guided Data Analysis Tutorial from GeekstoGeeks article: [Zomato Data Analysis Using Python](https://www.geeksforgeeks.org/data-analysis/zomato-data-analysis-using-python/)

The goal is to analyze Zomato restaurant data to extract meaningful insights about customer preferences. restaurant trends, and pricing behaviour using Python.

## Objectives
- Understand customer preferences in restaurants
- Analyze online vs offline ordering trends
- Identify popular restaurant types
- Explore rating distributions
- Determine preferred price ranges for couples
- Compare performance between different restaurant categories

## Technologies Used
- **Python**
- **Pandas** for Data Manipulation
- **Matplotlib** for Data Visualization
- **Seaborn** for Statistical Visualization

## Project Workflow
1. Import Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

2. Data Loading 
Read dataset using `read_csv()` and preview using `df.head()`
```python
df = pd.read_csv("Zomato-data-.csv")
```

3. Data Cleaning
Convert rating column into numeric format and handle string values like "4.2/5" and then check for null or missing values
```python
def handleRate(value):
    value = str(value).split('/')
    return float(value[0])

df['rate'] = df['rate'].apply(handleRate)
```

4. Exploratory Data Analysis (EDA)
**📊 Restaurant Types**
Most restaurants fall under Dining category
**🗳️ Votes Analysis**
Dining restaurants receive the highest number of votes
**⭐ Ratings Distribution**
Most ratings are between 3.5 and 4
**💻 Online Orders**
Majority of restaurants do not offer online ordering
**💰 Cost for Couples**
Preferred price range ≈ 300 (local currency)

## Key Insights 
- **Dining Restaurant** dominate the market
- Online ordering is less common but tends to have higher ratings
- Customer prefer mid-range pricing
- Cafes are more likely to receive online orders
- Offline dining still remains popular

## How to run the project
1. Clone the repository.
```bash 
git clone https://github.com/flylicenice/Zomato-Data-Analysis-with-Python.git
```

2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn
```

3. Run the notebook / script
```bash
python zomato-analysis.py
```

## 📚 What I Learned
- How to clean messy data (string to numeric)
- How to visualize data using seaborn
- How to extract business insights from datasets
