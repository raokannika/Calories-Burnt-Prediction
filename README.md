# Calories Burnt Prediction using Machine Learning

## Project Overview

This project focuses on predicting the **number of calories burned during physical exercise** using machine learning techniques.
The prediction is based on physiological and workout-related parameters such as **age, gender, duration, heart rate, and body temperature**.

The project follows a complete **end-to-end Machine Learning workflow**, starting from data collection to model evaluation.

---

## Datasets Used

This project uses **two datasets**, which are merged using a common `User_ID`.

### `exercise.csv`

Contains **exercise and body-related information** of users.

**Columns:**

* `User_ID` – Unique identifier for each user
* `Gender` – Male or Female
* `Age` – Age of the user
* `Height` – Height (in cm)
* `Weight` – Weight (in kg)
* `Duration` – Exercise duration (in minutes)
* `Heart_Rate` – Average heart rate during exercise
* `Body_Temp` – Body temperature during exercise

This dataset provides **input features** for prediction.

---

### `calories.csv`

Contains the **target variable**.

**Columns:**

* `User_ID` – Unique identifier
* `Calories` – Calories burnt during exercise

This dataset provides the **output (label)** for the model.

---

## Data Merging

Both datasets are combined using the `User_ID` column to create a single dataset for analysis and modeling.

---

## Project Workflow

The project follows the steps below:

1. **Data Collection**

   * Loaded datasets using Pandas

2. **Data Preprocessing**

   * Merged datasets
   * Checked for missing values
   * Converted categorical data (`Gender`) into numerical values

3. **Data Analysis & Visualization**

   * Statistical analysis using `describe()`
   * Distribution plots for features
   * Correlation analysis using a heatmap

4. **Feature & Target Separation**

   * Features (`X`) → Exercise and body parameters
   * Target (`Y`) → Calories burnt

5. **Train-Test Split**

   * Dataset split into **80% training** and **20% testing**

6. **Model Training**

   * Trained using **XGBoost Regressor**

7. **Model Evaluation**

   * Evaluated using **Mean Absolute Error (MAE)**

---

## Model Used – XGBoost Regressor

**XGBoost (Extreme Gradient Boosting)** is a powerful ensemble learning algorithm based on decision trees.

### Why XGBoost?

* Handles non-linear relationships effectively
* Works very well with structured/tabular data
* Reduces overfitting using regularization
* Provides high accuracy with efficient computation

The model was trained using default parameters and evaluated on unseen test data.

---

## Model Performance

* **Evaluation Metric:** Mean Absolute Error (MAE)
* **Achieved MAE:** ~**1.4 – 1.6**

This means the model’s calorie predictions differ from the actual values by **only about 1.5 calories on average**, indicating strong predictive performance.

---

## Technologies & Libraries Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost

---

## Conclusion

This project demonstrates a complete machine learning pipeline for regression problems using real-world fitness data.
The low error value shows that physiological and exercise parameters can effectively predict calorie expenditure when modeled correctly.

---
