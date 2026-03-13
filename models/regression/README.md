# Car Price Prediction Project 🚗📊

## Overview

This project focuses on building a **car price prediction model** using machine learning techniques. The goal is to predict the price of a car based on its features by applying regression models and proper data preprocessing techniques.

The project explores **Linear Regression, Ridge Regression, and Lasso Regression** while performing feature selection and regularization to improve model performance.

---

## Dataset

The dataset contains information about different cars and their attributes such as engine specifications, fuel efficiency, popularity, and other characteristics that influence vehicle pricing.

---

## Project Workflow

### 1. Data Exploration (EDA)

Basic **Exploratory Data Analysis (EDA)** was performed to understand the dataset structure and relationships between variables. This included:

* Checking dataset shape and data types
* Identifying missing values
* Visualizing feature distributions
* Investigating relationships between features and the target variable
* Detecting potential outliers

---

### 2. Data Preprocessing

Several preprocessing steps were applied before training the models:

**Handling Categorical Variables**

* Categorical variables were converted into numerical format using  **dummy variables (one-hot encoding)** .

**Handling Rare Categories**

* Car models with **less than 50 occurrences** were grouped into an  **"Other" category** .
* This was done **before splitting the dataset** to ensure that each category appears in all dataset splits.

**Feature Scaling**

* Numerical features were scaled using **StandardScaler** to normalize the feature distributions and improve model stability.

---

### 3. Dataset Splitting

The dataset was split into three parts:

* **Training Set:** 60%
* **Validation Set:** 20%
* **Test Set:** 20%

This allows:

* Training the model
* Tuning hyperparameters using the validation set
* Evaluating final model performance on the test set

---

### 4. Feature Selection

Feature selection was performed using  **Lasso Regression** .
Lasso introduces  **L1 regularization** , which can shrink some coefficients to zero, effectively removing less important features from the model.

This helps:

* Reduce overfitting
* Improve interpretability
* Identify the most important predictors of car price

---

### 5. Models Implemented

The following regression models were trained and compared:

#### Linear Regression

* Baseline model for predicting car prices.

#### Ridge Regression

* Uses **L2 regularization** to reduce model variance and prevent overfitting.

#### Lasso Regression

* Uses **L1 regularization** to perform automatic feature selection.

---

### 6. Model Evaluation

Models were evaluated using common regression metrics such as:

* **RMSE (Root Mean Squared Error)**
* **Validation performance**
* **Test set performance**

The validation set was used to tune model parameters, while the test set was used for final evaluation.

---

## Tools and Libraries Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib / Seaborn
* Jupyter Notebook

---

## Key Takeaways

* Proper **feature preprocessing** is essential for reliable model performance.
* **Regularization techniques** like Ridge and Lasso help prevent overfitting.
* **Handling rare categories** improves model robustness.
* Using a **train/validation/test split** ensures fair model evaluation.

---

## Future Improvements

Possible improvements to this project include:

* Hyperparameter tuning using **GridSearchCV**
* Trying more advanced models (Random Forest, Gradient Boosting, XGBoost)
* Feature engineering for additional predictive variables
* Model deployment as an API or web application
