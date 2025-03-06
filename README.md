# House Prices Prediction - Advanced Regression Techniques

## Overview

This project focuses on predicting house prices using advanced regression techniques applied to the Ames, Iowa housing dataset. The dataset contains 79 explanatory variables describing various aspects of residential properties, aiming to provide actionable insights for real estate professionals, investors, and prospective homebuyers.

## Project Objectives

*   Understand variable distributions and interactions within the dataset.
*   Apply data transformations to enhance model performance and interpretability.
*   Utilize visualization techniques to uncover patterns and understand variable distributions.
*   Accurately predict sale prices of homes in the test dataset.
*   Synthesize and communicate valuable insights to stakeholders.

## Data Source

The Ames, Iowa housing dataset was obtained from a Kaggle competition: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

## Methodology

1.  **Data Loading and Exploration:**
    *   Loaded training and test datasets into Google Colab.
    *   Examined variables, focusing on missing values (NA).
    *   Analyzed the distribution of the 'SalePrice' variable.
    *   Reviewed variable counts and data types.

2.  **Data Cleaning:**
    *   Removed columns with more than 81 missing values from the training data.
    *   For categorical data, NA values were replaced using a weighted average methodology.
    *   For numerical data, NA values were replaced with the column's average value.
    *   Specific columns like 'GarageType' and 'GarageYrBlt' were imputed using averages of similar types or the column average, respectively.

3.  **Data Visualization:**
    *   Plotted graphs to visualize relationships between variables and 'SalePrice'.
    *   Used heatmaps to show variable interactions.
    *   Created scatter plots to identify patterns between specific variables and sale prices.

4.  **Data Preprocessing:**
    *   Transformed categorical variables into numerical format using OneHotEncoder.
    *   Created a preprocessing pipeline using ColumnTransformer to handle categorical variables while preserving numerical features.

5.  **Model Implementation and Training:**
    *   Two separate pipelines were established:
        *   **Random Forest Pipeline:** Included the preprocessor and a Random Forest Regressor.
        *   **XGBoost Pipeline:** Included the preprocessor and an XGB Regressor with specific hyperparameters.
    *   The dataset was split into training (70%) and validation (30%) sets.
    *   Models were trained using the training data and evaluated on the validation set.

6.  **Model Selection:**
    *   Started with a basic Logistic Regression model, which performed poorly.
    *   Improved performance with a Random Forest model.
    *   Further enhanced the Random Forest model by allowing bootstrapping to control overfitting.
    *   Experimented with an XGBoost model, which yielded similar performance to the Random Forest model but lacked overfitting control.
    *   Finalized Random Forest with bootstrapping as the best model.

