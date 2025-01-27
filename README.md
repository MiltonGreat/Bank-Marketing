# Bank Marketing Campaign Analysis

## Project Overview

This project focuses on analyzing and modeling data from a bank marketing campaign. The goal is to predict whether a client will subscribe to a term deposit based on demographic, financial, and campaign-related features. The dataset includes over 45,000 records with features such as age, job, education, marital status, and campaign duration.

### Key Objectives

1. **Data Cleaning and Preprocessing**:
   - Handle missing values and outliers.
   - Normalize numerical features for consistency.
   - Encode categorical features using one-hot and label encoding.

2. **Exploratory Data Analysis (EDA)**:
   - Understand data distribution and relationships among features.
   - Identify patterns and anomalies in customer and campaign behavior.

3. **Predictive Modeling**:
   - Train a Logistic Regression model to classify customer responses.
   - Evaluate model performance using metrics like accuracy, precision, recall, and F1-score.

## Dataset

The dataset is available in the `Bank Marketing Dataset.zip` file, which includes:
- `bank-full.csv`: The primary dataset with all records.
- `bank.csv`: A smaller subset of the data for quick testing.
- `bank-names.txt`: Feature descriptions and metadata.

### Features

- **Demographics**: `age`, `job`, `marital`, `education`
- **Financial Information**: `balance`, `loan`, `housing`, `default`
- **Campaign Data**: `duration`, `campaign`, `pdays`, `previous`
- **Outcome**: `y` (Target variable: `1` for subscription, `0` otherwise)

## Key Steps

#### 1. Data Cleaning
- Imputed missing values using median for numerical features and mode for categorical features.
- Removed leading/trailing spaces in column names.
- Normalized numerical columns using `StandardScaler`.
- Encoded binary and categorical columns using `LabelEncoder` and one-hot encoding.

#### 2. Exploratory Data Analysis (EDA)
- Summary statistics and distributions for numerical and categorical variables.
- Visualizations:
  - Distribution of campaign durations and balances.
  - Analysis of customer age and campaign success rates.

#### 3. Predictive Modeling
- **Logistic Regression**:
  - Handled imbalanced classes using `class_weight='balanced'`.
  - Evaluated performance on a test set using:
    - **Accuracy**: `88%`
    - **Precision, Recall, F1-score** for both classes.
    - Confusion matrix for detailed error analysis.

### Results

The model achieved an accuracy of 88% with the following performance metrics:

- Precision (no): 0.93
- Recall (no): 0.94
- Precision (yes): 0.50
- Recall (yes): 0.45
- F1-Score (yes): 0.48
- Overall Accuracy: 0.88

Although the accuracy is high, the model is biased towards predicting the 'no' class due to the imbalance in the target variable. Further steps can be taken to address this, such as tuning the model, trying different sampling methods, or using algorithms that handle class imbalance better.

### Source

https://www.kaggle.com/datasets/hariharanpavan/bank-marketing-dataset-analysis-classification
