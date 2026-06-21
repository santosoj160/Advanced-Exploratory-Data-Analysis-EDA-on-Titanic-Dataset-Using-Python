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
## Visualizations

### 1. Survival Rate by Passenger Class

Heatmap showing the percentage of passengers who survived based on passenger class.

![Survival Rate by Passenger Class](images/survival_rate_by_pclass.png)

---

### 2. Survival Rate by Gender

Heatmap illustrating the survival percentage between male and female passengers.

![Survival Rate by Gender](images/survival_rate_by_gender.png)

---

### 3. Average Age by Gender and Survival Status

Heatmap showing the average age of passengers grouped by gender and survival outcome.

![Average Age by Gender and Survival](images/average_age_by_gender_survival.png)

---

### 4. Passenger Count by Gender and Survival Status

Heatmap displaying the absolute number of passengers by gender and survival status.

![Passenger Count by Gender and Survival](images/passenger_count_by_gender_survival.png)

---

### 5. Average Age by Gender

Bar chart comparing the average age of male and female passengers.

![Average Age by Gender](images/average_age_by_gender_barplot.png)
---

## Key Findings

### 1. Gender Was the Strongest Survival Indicator

The survival rate among female passengers was significantly higher than that of male passengers across all passenger classes. This pattern suggests that gender played a critical role in determining survival outcomes during the disaster.

### 2. Socioeconomic Status Influenced Survival Probability

Passenger class showed a strong relationship with survival. First-class passengers achieved the highest survival rates, while third-class passengers experienced the lowest. This indicates that socioeconomic status may have affected access to lifeboats and emergency resources.

### 3. Combined Effect of Gender and Passenger Class

The analysis revealed that female passengers in higher classes had the greatest likelihood of survival, whereas male passengers in lower classes faced the highest mortality rates. This demonstrates that survival was influenced by the interaction of multiple demographic factors rather than a single variable.

### 4. Passenger Distribution Was Highly Imbalanced

The dataset contained a considerably larger number of male non-survivors compared to other groups. This imbalance highlights the importance of examining both absolute counts and percentage-based metrics when interpreting survival patterns.

### 5. Age Showed a Moderate Relationship with Survival

Average age differences between survivors and non-survivors suggest that age may have contributed to survival outcomes. However, its influence appears weaker than the effects of gender and passenger class.

### 6. Survival Outcomes Were Not Random

Cross-tabulation and aggregation analyses consistently demonstrated systematic patterns across demographic groups. The findings indicate that survival was associated with identifiable passenger characteristics rather than occurring by chance alone.

### 7. Potential Features for Predictive Modeling

Based on the exploratory analysis, variables such as Gender (Sex), Passenger Class (Pclass), Age, and Fare are likely to be valuable predictors for machine learning models designed to estimate survival probability.


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
