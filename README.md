# Loan Approval Prediction using Machine Learning

## Project Overview

This project focuses on predicting loan approval decisions based on applicants' demographic, financial, and credit-related information.

The project includes exploratory data analysis, data preprocessing, handling missing values, feature transformation, model training, hyperparameter tuning, and model evaluation.

## Dataset

The dataset contains information about loan applicants, including:

- Gender
- Marital Status
- Number of Dependents
- Education
- Self-Employment Status
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area
- Loan Status

The target variable is **Loan_Status**, which indicates whether the loan was approved or rejected.

## Project Workflow

### 1. Exploratory Data Analysis

The dataset was explored to understand:

- Data types and distributions
- Missing values
- Categorical variables
- Numerical variables
- Distribution of important features
- Potential outliers

### 2. Data Preprocessing

The preprocessing steps included:

- Handling missing values
- Encoding categorical variables
- Examining potential outliers
- Applying transformations to skewed numerical features
- Preparing the data for machine learning models

For example, logarithmic transformation was applied to skewed income-related features to reduce the influence of extreme values.

### 3. Data Splitting

The dataset was divided into:

- Training set
- Validation set
- Test set

The test set was kept separate for final model evaluation.

### 4. Machine Learning Models

Three classification algorithms were implemented and compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Artificial Neural Network (ANN)

Both scaled and non-scaled data were evaluated to investigate the effect of feature scaling on model performance.

### 5. Model Evaluation

The models were evaluated using several classification metrics, including:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- False Positives

Special attention was given to **Recall and False Positive (FP)** because of their importance in the loan approval context.

### 6. Model Improvement

Hyperparameter tuning was performed to improve model performance.

For the ANN model, different hyperparameters such as:

- Hidden layer sizes
- Activation function
- Alpha
- Learning rate

were investigated using `GridSearchCV`.

The maximum number of iterations was also increased to examine its effect on ANN convergence and performance.

## Results

The models were compared on both scaled and non-scaled data.

Based on the business objective of maintaining high recall while controlling false positives, the models showed different trade-offs.

On the scaled data, KNN provided a good balance between recall and false positives, making it a suitable model under the defined evaluation criteria.

Further analysis and hyperparameter tuning were performed to investigate possible improvements.

## Key Takeaways

- Missing values can significantly affect machine learning models and should be handled carefully.
- Feature transformations can help reduce the effect of highly skewed numerical variables.
- Feature scaling does not necessarily improve every machine learning model.
- Model selection should consider the business objective and not rely only on accuracy.
- Recall and False Positive rates can be particularly important in financial classification problems.
- Hyperparameter tuning can improve model performance and provide a better understanding of model behavior.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
loan-approval-prediction/
│
├── README.md
├── notebooks/
│   └── Loan_Approval_Prediction.ipynb
│
├── data/
│   └── loan_data.csv
│
└── requirements.txt
