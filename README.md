README.md

This repository contains Python code for predicting sales in a retail scenario. The main components of the project are:

-------------------------------------1. Data Cleaning and Preprocessing (`1. bigmart_EDA.ipynb`)-------------------------------------
    - Reads the training data (`train.csv`).
    - Handles missing values for `Item_Weight`, `Outlet_Size`, and `Item_Visibility`.
    - Analyzes and visualizes data using KDE plot and box plots.
    - Replaces categorical values with numerical values.
    - Saves the processed data to `train_data.csv`.
    - Saves label encoder instances for future use.



-------------------------------------2. Model Development (`2. bigmart_modeldev.ipynb`)-------------------------------------
    - Imports necessary libraries.
    - Reads the processed training data.
    - Splits the data into features (X) and the target variable (y).
    - Applies various regression models: Linear Regression, Ridge Regression, Lasso Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost, 	LightGBM, and CatBoost.
    - Conducts hyperparameter tuning using GridSearchCV for Gradient Boosting.
    - Saves the best model using joblib.
    - Evaluates and prints the RMSE for each model.
    - Extracts feature importance from the Gradient Boosting model.
    - Prints and visualizes feature importance.



-------------------------------------3. Test Data Processing (`bigmart_testdatacleaning.ipynb`)-------------------------------------
    - Reads the test data (`test.csv`).
    - Applies the same data preprocessing steps as the training data.
    - Saves the processed test data to `test_data.csv`.
    - Saves label encoder instances for future use.



-------------------------------------4. Sales Prediction (`bigmart_modeltest.ipynb`)-------------------------------------
    - Reads the processed test data.
    - Loads the best Gradient Boosting model.
    - Takes user input for a single instance and predicts the sales.
    - Demonstrates how to calculate the absolute difference and percentage error between predicted and actual values.
    - Applies the model to predict sales for the entire test data.
    - Reverses label encoding and saves the predictions to `test_file_with_predictions.csv`.


Notes:
Please note that the code assumes the presence of the necessary data files (`train.csv` and `test.csv`). The data files should be in the same directory as the notebooks. The processed and predicted data files (`train_data.csv` and `test_file_with_predictions.csv`) will be generated in the same directory.

Make sure to install the required libraries before running the code by executing `pip install catboost` in your environment.