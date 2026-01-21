# Lung Cancer Prediction Using Logistic Regression with Snowflake Data

This project builds a Logistic Regression model to predict lung cancer using
survey data stored in a Snowflake data warehouse. The workflow includes data
extraction, preprocessing, model training, evaluation, and model persistence.

---

## Project Description

The dataset is fetched directly from Snowflake using the Snowflake Python
connector. After inspecting the data, categorical variables are encoded and
numerical features are scaled. A Logistic Regression model is then trained to
classify lung cancer cases. The model performance is evaluated using standard
classification metrics and ROC-AUC score.

The trained model and scaler are saved for future inference.

---

## Data Source

- Platform: Snowflake
- Database: User-defined
- Schema: PUBLIC
- Table: Lung cancer survey table

Data is retrieved using SQL queries and loaded into a Pandas DataFrame.

---

## Tools and Libraries Used

- Python
- Pandas
- Snowflake Connector for Python
- Scikit-learn
- Joblib

---

## Workflow

1. Connect to Snowflake
2. Fetch data using SQL
3. Perform data inspection
4. Encode categorical variables
5. Scale numerical features using StandardScaler
6. Split data into training and testing sets
7. Train Logistic Regression model
8. Evaluate model performance
9. Save trained model and scaler

---

## Model Details

- Algorithm: Logistic Regression
- Class balancing: Enabled
- Maximum iterations: 1000
- Evaluation metrics:
  - Precision
  - Recall
  - F1-score
  - ROC-AUC

---

## Results

The model demonstrates good performance in classifying lung cancer cases.
ROC-AUC score is used to measure the model’s ability to distinguish between
classes.

---

## Model Artifacts

- `logisticregr.joblib` – Trained Logistic Regression model
- `scaler.joblib` – Fitted feature scaler

---

## How to Run the Project

1. Clone the repository
2. Install required libraries
   ```bash
   pip install pandas scikit-learn snowflake-connector-python joblib
