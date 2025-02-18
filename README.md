# Bank Marketing Campaign - Subscription Prediction

## Project Overview

This project analyzes data from a bank marketing campaign to predict whether a client will subscribe to a term deposit. The dataset includes demographic, financial, and campaign-related features from over 45,000 records. The primary objective is to build predictive models that are sensitive to the class imbalance between subscribers and non-subscribers.

### Key Objectives

1. **Data Cleaning and Preprocessing**:
   - Handle missing values and outliers.
   - Normalize numerical features for consistency.
   - Encode categorical features using one-hot and label encoding.

2. **Exploratory Data Analysis (EDA)**:
   - Understand data distribution and relationships among features.
   - Identify patterns and anomalies in customer and campaign behavior.

3. **Predictive Modeling**:
   - Train and evaluate classification models such as Logistic Regression, Random Forest, and XGBoost.
   - Address class imbalance using SMOTE and hyperparameter tuning.
   - Assess model performance using precision, recall, F1-score, and ROC-AUC.

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

#### Performance Metrics

After applying SMOTE to address class imbalance, the models demonstrated:

Random Forest (with SMOTE):
- Precision (yes): 0.48
- Recall (yes): 0.32
- F1-Score (yes): 0.38
- ROC-AUC Score: 0.6348
- Overall Accuracy: 88%

XGBoost (with SMOTE):
- Precision (yes): 0.47
- Recall (yes): 0.34
- F1-Score (yes): 0.40
- ROC-AUC Score: 0.6455
- Overall Accuracy: 87%

### Key Findings

- Both models show strong performance for predicting non-subscribers (Class 0), with high precision and recall.
- Performance for subscribers (Class 1) remains a challenge. While SMOTE improved recall for the minority class, there is still significant room for improvement, as precision and recall remain relatively low for this class.
- The ROC-AUC scores suggest that while both models perform better than random guessing, their ability to differentiate between the two classes can still be optimized.

### Conclusion

This project has demonstrated the importance of addressing class imbalance when predicting minority classes, such as customer subscriptions to a term deposit. While SMOTE improved the recall for subscribers, further optimization is needed to improve overall model sensitivity for predicting this minority class. Techniques like undersampling, cost-sensitive learning, and hyperparameter tuning should be explored in future iterations to refine the model's ability to accurately predict both classes.
  
### Source

Dataset: [Bank Marketing Campaign Analysis Dataset on Kaggle](https://www.kaggle.com/datasets/hariharanpavan/bank-marketing-dataset-analysis-classification)
