# Internship_Fusion_EDAProject


## Titanic Survival Prediction - Data Preparation and Analysis

### Project Overview

This project involves preparing the Titanic dataset for a machine learning model that predicts passenger survival based on various factors. We perform the following tasks in this part of the project:

### Data Cleaning: 
Handling missing data and correcting data types.

### Feature Engineering: 
Creating new features to enrich the dataset.

### Exploratory Data Analysis (EDA): 
Understanding relationships between features and survival using visualizations.

### Project Files

train.csv: The training dataset used for analysis and modeling.

test.csv: The test dataset used for model evaluation.

data_preprocessing.ipynb: Jupyter notebook containing the code for data cleaning, feature engineering, and EDA.

README.md: Documentation of the tasks and project structure.

### Data Cleaning

The raw Titanic dataset contains some missing or inconsistent values that need to be addressed before modeling. The following steps were taken to clean the data:

### Handling Missing Values:

Age: Missing values were filled with the median age of the passengers.

Cabin: Missing cabin values were replaced with the string 'Unknown'.

Embarked: Missing values were filled with the mode (most frequent value).

Fare: Missing values in the test dataset were filled with the median fare.

### Data Type Corrections:

Ensured all categorical features (e.g., Sex, Embarked, Title) were properly encoded into numerical values for modeling.

### Feature Engineering

To improve the predictive power of the model, several new features were created from existing data:

FamilySize: The total number of family members traveling with the passenger was calculated using the sum of SibSp (siblings/spouses) and Parch (parents/children), plus one for the passenger.

IsAlone: A binary feature indicating if the passenger was traveling alone (1 for alone, 0 otherwise).

Title: Titles (e.g., Mr., Mrs., Miss) were extracted from the Name feature to capture social status and used to create a new categorical variable. Rare titles were grouped together into an "Other" category.

### Exploratory Data Analysis (EDA)

EDA was conducted to understand the relationships between features and passenger survival. Key visualizations and insights include:

### Survival Rates by Passenger Class:

Higher-class passengers (1st class) had a higher survival rate compared to lower-class passengers.
Survival Rates by Gender:

Female passengers had a significantly higher survival rate compared to males.
Family Size Impact:

Passengers traveling alone (IsAlone == 1) had a lower chance of survival compared to those traveling with family members.
Title-based Survival:

Certain titles such as "Miss" and "Mrs" had higher survival rates.
