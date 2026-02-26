# EDA_EXP_4   Titanic Survival Analysis using Univariate Analysis

## Aim

To perform univariate analysis on the Titanic dataset to understand the distribution and characteristics of individual variables (such as Age, Sex, Pclass, Fare, and Survived) and to draw insights about passengers and their survival patterns.

## Algorithm

### 1)Import Libraries:

Load the required Python libraries (pandas, numpy, matplotlib, seaborn).

### 2)Load the Dataset:

Read the Titanic dataset from available sources (e.g., seaborn’s built-in Titanic dataset or a CSV file).

### 3)Data Inspection:

View the first few rows using head().

Get dataset summary using info() and describe().

### 4)Handle Missing Data:
Identify missing values using isnull().sum() and handle them appropriately (e.g., fill or drop).

### 5)Univariate Analysis:
Perform univariate analysis for each variable:

#### Categorical Variables: (e.g., Sex, Pclass, Survived, Embarked)
Use frequency tables and count plots.

#### Numerical Variables: (e.g., Age, Fare)
Use histograms, box plots, and summary statistics.

### 6)Interpretation:
Analyze distributions, central tendencies, and spread.
Identify patterns (e.g., more passengers in 3rd class, survival differences by gender).


### Program

#### Name :

#### Reg No.:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = sns.load_dataset("titanic")
df.head()

df.shape

df.isnull().sum()
```

```python
df["sex"].value_counts()

sns.countplot(x='sex', data=df)
plt.title("Distribution of Gender")
plt.show()

df["survived"].value_counts(normalize=True) * 100
df["pclass"].value_counts()
df['embarked'].value_counts()
df["deck"].value_counts()
```

### Output
<img width="1107" height="215" alt="image" src="https://github.com/user-attachments/assets/7568d697-06c9-4e4b-b148-7c5f3147e6d0" />

<img width="184" height="28" alt="image" src="https://github.com/user-attachments/assets/209a62b2-1afa-41d7-bbda-92037f1f4e85" />

<img width="428" height="605" alt="image" src="https://github.com/user-attachments/assets/345b7be7-24cd-4a00-8f27-a9168a3b0ae5" />


### Result

From the univariate analysis: 

Majority of passengers were male and in 3rd class.

Around 38% survived, majority being females and higher-class passengers.

Age is right-skewed with most passengers aged 20–40 years.

Fare distribution shows a few high outliers for 1st class passengers.

Thus, univariate analysis helps understand the distribution and spread of each individual feature in the Titanic dataset before moving to bivariate or multivariate analysis.

Visualization:
Plot appropriate charts for each variable using Matplotlib/Seaborn.
