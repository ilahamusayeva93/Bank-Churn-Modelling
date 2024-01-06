# Bank Churn Modelling

## Overview

This repository contains an R Notebook for churn analysis on a bank's customer dataset. The analysis involves data exploration, preprocessing, building a churn prediction model, comparing results on training and test sets, and evaluating the model using ROC and AUC curves.

## Notebook Details

### 1. Data Exploration and Preparing for Modelling

- **Libraries:** The script loads necessary R libraries for data manipulation, exploratory data analysis, model building, and visualization.

- **Data Loading:** The dataset "bank_full.csv" is loaded using the `data.table` library.

- **Exploration:** The script explores the dataset using functions like `glimpse`, `inspect_na`, and `View`.

- **Data Cleaning:** Unneeded columns ('contact', 'education', 'marital') are removed, and the target variable 'y' is converted to a binary factor.

- **Information Value (IV) Analysis:** IV is calculated for variable selection based on a threshold of 0.02.

- **Binning:** Binning is performed on the selected variables.

- **Outlier Handling:** Outliers in numeric variables are identified and handled.

- **Dummy Variable Creation:** Dummy variables are created for character variables.

- **Train-Test Split:** The dataset is split into training and testing sets.

- **WoE Transformation:** Weight of Evidence (WoE) transformation is applied on training and testing sets.

### 2. Modeling

- **Variable Selection:** Logistic regression model is built using the `glm` function.

- **Model Refinement:** Non-significant variables are iteratively removed based on p-values.

- **H2O GLM Model:** An H2O GLM model is built with variable selection and removal of collinear columns.

### 3. Model Evaluation

- **Model Predictions:** Predictions are made on the test set using the H2O model.

- **Performance Evaluation:** Model performance is evaluated using H2O's performance metrics, including precision, AUC, Gini, and confusion matrix.

- **ROC & AUC Curves:** ROC curves are generated, and the threshold for the max F1 score is identified. AUC and Gini values for train, test, and cross-validation are displayed.

## Dataset Information

### Description

The dataset contains information about bank customers, and the goal is to predict churn based on various features.

### Analysis Tasks

1. **Data Import:** Import the "bank_full.csv" dataset.
2. **Remove Unneeded Columns:** Remove unnecessary columns identified during data exploration.
3. **Build Churn Model:** Build a logistic regression model and refine it.
4. **Compare Model Results:** Compare model results on training and test sets.
5. **Evaluate Model Results:** Evaluate and explain model results using ROC and AUC curves.

## How to Use

To replicate the analysis:

1. Ensure you have R and the required libraries installed.
2. Place the "bank_full.csv" dataset in the same directory as the notebook.
3. Run the notebook in an R environment, considering any specific package dependencies.

## Author

- **Author:** Ilaha Musayeva
- **Date:** 11.21.2023


