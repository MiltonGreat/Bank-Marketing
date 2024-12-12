# Bank Marketing Dataset

### Overview

This project uses the Bank Marketing Dataset to practice preprocessing steps like one-hot encoding for categorical features and normalization for numerical features, in order to prepare the data for machine learning models. The dataset consists of marketing campaign data from a Portuguese banking institution, and the goal is to predict whether a client will subscribe to a term deposit (y column).

### Project Overview

The goal of this project is to predict whether a customer will subscribe to a term deposit based on various attributes like:

- Demographic information (e.g., age, job, marital status)
- Previous marketing campaign data (e.g., contact, duration, campaign)
- Financial data (e.g., balance, housing, loan)

Since this is a highly imbalanced dataset, careful consideration was given to preprocessing, encoding, and model evaluation to deal with the imbalance between the two target classes (subscribed or not subscribed to a term deposit).

### Data Preprocessing

- Handling Missing Values: Missing values are imputed with the median for numerical features and the mode for categorical features.
- One-Hot Encoding: Categorical columns like job, marital, education, contact, month, and poutcome are one-hot encoded to transform them into binary variables.
- Label Encoding: Binary columns like loan, housing, and default are label encoded to convert yes to 1 and no to 0.
- Normalization: Numerical features like age, balance, duration, campaign, pdays, and previous are normalized using StandardScaler to ensure the features are on a similar scale.
- Feature Engineering: The target variable y is encoded to 1 for 'yes' and 0 for 'no'.

### Model Training and Evaluation

A Logistic Regression model was trained on the preprocessed data.

### Results

Here are the results from the Logistic Regression model: Accuracy: 0.84

### Source

https://www.kaggle.com/datasets/hariharanpavan/bank-marketing-dataset-analysis-classification
