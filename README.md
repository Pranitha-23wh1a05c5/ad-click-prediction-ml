# ad-click-prediction-ml

# Ad Click Prediction using Machine Learning

##  Project Overview

This project focuses on predicting whether a user will click on an advertisement based on demographic, device, and contextual features. The goal is to understand which factors most strongly influence ad engagement and to compare different machine learning models for this task.

The project simulates a real-world advertising scenario similar to large-scale ad platforms, emphasizing data preprocessing, model evaluation, and interpretability.


## Problem Statement

Given user and ad context information such as age, device type, ad position, browsing history, and time of day, predict whether the user will click on an advertisement (click=1) or not (click = 0).


##  Dataset Description

The dataset contains **10,000 records** with the following key features:

* **age** – User age
* **gender** – Gender of the user
* **device_type** – Device used (Mobile, Tablet, etc.)
* **ad_position** – Placement of the ad (Top, Side, etc.)
* **browsing_history** – User browsing behavior category
* **time_of_day** – Time when the ad was shown
* **click** – Target variable (0 = No Click, 1 = Click)

Non-informative columns such as user ID and name were removed during preprocessing.

##  Tech Stack

* **Language:** Python
* **Environment:** Google Colab
* **Libraries:**

  * pandas, NumPy
  * scikit-learn
  * matplotlib, seaborn


##  Project Workflow

1. Data loading and inspection
2. Handling missing values (median for numerical, “Unknown” for categorical)
3. One-hot encoding of categorical variables
4. Feature scaling using StandardScaler
5. Model training and evaluation
6. Model comparison and feature importance analysis


##  Models Used

###  Logistic Regression

* Used as a baseline classification model
* Simple and interpretable
* Assumes linear relationship between features and click probability

###  Random Forest Classifier

* Ensemble-based, non-linear model
* Captures complex feature interactions
* Provides feature importance for interpretability


##  Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* ROC-AUC Score

Random Forest achieved a higher ROC-AUC compared to Logistic Regression, indicating better performance in ranking users by click probability.

##  Key Insights

* **Age** was the most influential predictor of ad clicks
* **Device type** and **ad position** significantly impacted user engagement
* **Gender** and **time of day** provided additional but smaller contributions
* Random Forest outperformed Logistic Regression by capturing non-linear patterns in user behavior

##  Feature Importance Analysis

Feature importance from the Random Forest model showed that demographic and contextual signals play a major role in ad engagement, highlighting the importance of personalization and placement in advertising systems.


##  Conclusion

This project demonstrates how machine learning can be applied to advertising data to predict user engagement and extract meaningful business insights. Comparing linear and ensemble models helped highlight the importance of non-linear feature interactions in real-world ad click prediction tasks.


##  Future Improvements

* Hyperparameter tuning
* Trying gradient boosting models (XGBoost, LightGBM)
* Handling class imbalance using advanced sampling techniques
* Model deployment as a simple API
