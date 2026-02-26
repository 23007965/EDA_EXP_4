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

##### Data Understanding
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = sns.load_dataset("titanic")
df.head()

df.shape

df.isnull().sum()
```
##### Categorical Variable Analysis
```python
df["sex"].value_counts()

sns.countplot(x='sex', data=df)
plt.title("Distribution of Gender")
plt.show()
```
```python
print("percentage of passengers survived")
df["survived"].value_counts(normalize=True) * 100
```
```python
df["pclass"].value_counts()

sns.countplot(x='pclass', data=df)
plt.title("Passenger class distribution")
plt.show()
```
```python
df['embarked'].value_counts()

sns.countplot(x='embarked', data=df)
plt.title("passengers embarked from each port")
plt.show()
```
```python
df["deck"].value_counts()

sns.countplot(x='deck', data=df)
plt.title("Deck distribution")
plt.show()
```

### Output

<img width="1107" height="215" alt="image" src="https://github.com/user-attachments/assets/7568d697-06c9-4e4b-b148-7c5f3147e6d0" />

<img width="393" height="24" alt="image" src="https://github.com/user-attachments/assets/23862f5f-87a2-4b15-b2c3-c06af1c6f076" /><br><br>

<img width="385" height="629" alt="image" src="https://github.com/user-attachments/assets/350177d4-080e-4e55-8104-385af02f0aed" /><br><br>

<img width="539" height="181" alt="image" src="https://github.com/user-attachments/assets/94fd9979-cf9a-429a-8966-ec12f2c34007" /><br><br> 

<img width="767" height="503" alt="image" src="https://github.com/user-attachments/assets/976bfd04-aec3-4ac6-a8d7-58fe57886d2d" /><br><br>

<img width="576" height="206" alt="image" src="https://github.com/user-attachments/assets/6de3f352-127e-4e73-96a5-4f72273096eb" /><br><br>


### Result

From the univariate analysis: 

Majority of passengers were male and in 3rd class.

Around 38% survived, majority being females and higher-class passengers.

Age is right-skewed with most passengers aged 20–40 years.

Fare distribution shows a few high outliers for 1st class passengers.

Thus, univariate analysis helps understand the distribution and spread of each individual feature in the Titanic dataset before moving to bivariate or multivariate analysis.

Visualization:
Plot appropriate charts for each variable using Matplotlib/Seaborn.
