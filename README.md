# titanic_dataset

**README.md**

# Titanic Dataset Analysis

## Overview
This project involves an exploratory data analysis (EDA) of the Titanic dataset. The analysis aims to uncover insights regarding the passengers and their survival rates using various statistical and visualization techniques.

## Contents
- Data Loading
- Data Summary
- Missing Values Analysis
- Visualizations
- Correlation Analysis
- Observations

## Requirements
To run this project, you will need the following Python libraries:
- pandas
- matplotlib
- seaborn
- numpy

You can install the required libraries using pip:
```bash
pip install pandas matplotlib seaborn numpy
```

## Data Loading
The Titanic dataset is loaded from a CSV file:
```python
titanic_data = pd.read_csv('/content/drive/MyDrive/data/train.csv')
```

## Data Summary
The first few rows of the dataset and a summary of its structure are displayed using:
```python
print(titanic_data.head())
print(titanic_data.info())
print(titanic_data.describe())
```

## Missing Values Analysis
The analysis checks for missing values and visualizes them using a heatmap:
```python
sns.heatmap(titanic_data.isnull(), cbar=False, cmap='viridis')
```

## Visualizations
Several visualizations are created to understand the data better:
- Histograms for numerical features
- Boxplots for Age and Fare
- Pairplot to visualize relationships between features

## Correlation Analysis
A correlation matrix is calculated and visualized to identify relationships between numerical features:
```python
correlation_matrix = titanic_data[numeric_cols].corr()
sns.heatmap(correlation_matrix, annot=True, fmt='.2f', cmap='coolwarm')
```

## Observations
Key observations from the analysis are documented:
1. The majority of passengers were not survivors.
2. There are missing values in the Age and Cabin columns.
3. The Fare distribution is right-skewed.
4. There is a strong correlation between Pclass and Survived.
5. Age and Fare also show some correlation with survival.

## Output
The observations are saved to a text file named `titanic_eda_report.txt`.

## Acknowledgments
- The Titanic dataset is available from [Kaggle](https://www.kaggle.com/c/titanic/data).
