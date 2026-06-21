# Advanced-Exploratory-Data-Analysis-EDA-on-Titanic-Dataset-Using-Python
Advanced Exploratory Data Analysis (EDA) on Titanic Dataset using Python, Pandas, and Seaborn to uncover passenger survival patterns and data insights.

## Project Overview

This project demonstrates the application of Advanced Exploratory Data Analysis (EDA) techniques using the Titanic Dataset.

The analysis focuses on understanding passenger characteristics, survival patterns, and relationships between variables through filtering, sampling, cross-tabulation, and group-by aggregation techniques.

The objective is to extract meaningful insights from the dataset and strengthen data analysis skills using Python and Pandas.

---

## Dataset Information

Dataset: Titanic Dataset

Source:
https://www.kaggle.com/datasets/yasserh/titanic-dataset

Dataset contains passenger information such as:

* Passenger ID
* Survival Status
* Passenger Class
* Name
* Gender
* Age
* Fare
* Embarked Port
* Family Information

---

## Objectives

The project aims to:

* Understand the structure and quality of the dataset
* Perform advanced exploratory data analysis
* Identify patterns related to passenger survival
* Compare demographic characteristics across groups
* Generate business-style insights from data

---

## Tools and Libraries

### Python Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Environment

* Python
* Jupyter Notebook / Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## Analysis Workflow

### 1. Data Loading

Load Titanic dataset and inspect the structure.

```python
df.head()
df.info()
df.describe()
```

---

### 2. DataFrame Rows Filtering

Examples:

* Survived passengers
* Female survivors
* First-class passengers above 30 years old

```python
df[df['Survived'] == 1]
```

---

### 3. Sampling and Randomization

Random sampling for quick exploration.

```python
df.sample(
    n=10,
    random_state=42
)
```

Benefits:

* Faster exploration
* Reproducible analysis
* Efficient inspection of large datasets

---

### 4. Cross Tabulation

Analyze relationships between categorical variables.

Examples:

* Gender vs Survival
* Passenger Class vs Survival
* Embarked Port vs Survival

```python
pd.crosstab(
    df['Sex'],
    df['Survived']
)
```

---

### 5. Group-By Aggregation

Aggregate statistics by category.

Examples:

```python
df.groupby('Pclass').agg({
    'Age':['mean','max','min']
})
```

```python
df.groupby('Sex').agg({
    'Fare':['mean','sum']
})
```

Statistics used:

* Mean
* Median
* Sum
* Count
* Max
* Min

---

## Key Findings

### Survival by Gender

Female passengers had a significantly higher survival rate compared to male passengers.

### Survival by Passenger Class

Passengers in higher classes showed better survival rates than those in lower classes.

### Age Distribution

Most passengers were adults between 20 and 40 years old.

### Fare Analysis

Higher ticket fares were generally associated with higher passenger classes.

---

## Skills Demonstrated

* Data Cleaning
* Data Exploration
* Data Filtering
* Sampling Techniques
* Cross Tabulation
* Group By Aggregation
* Data Visualization
* Insight Generation
* Exploratory Data Analysis (EDA)

---

## Project Structure

```text
Titanic-Advanced-EDA/
│
├── data/
│   └── Titanic-Dataset.csv
│
├── notebooks/
│   └── Advanced_EDA_Titanic.ipynb
├── images/
│   ├── survival_rate_by_pclass.png
│   ├── survival_rate_by_gender.png
│   ├── average_age_by_gender_survival.png
│   ├── passenger_count_by_gender_survival.png
│   └── average_age_by_gender_barplot.png
│
└── README.md
```

---

## Conclusion

This project demonstrates how advanced exploratory data analysis techniques can be used to uncover meaningful patterns and relationships within the Titanic dataset.

Through filtering, sampling, cross-tabulation, and aggregation methods, valuable insights were obtained regarding passenger demographics and survival outcomes.

The project also strengthens practical skills required for Data Analyst roles, particularly in data exploration and insight generation.
