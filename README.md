README.md

This repository contains Python code for predicting sales in a retail scenario. The main components of the project are:

-------------------------------------1. Data Cleaning and Preprocessing ('1. bigmart_EDA.ipynb')-------------------------------------<br>
    - Reads the training data ('train.csv').<br>
    - Handles missing values for 'Item_Weight', 'Outlet_Size', and 'Item_Visibility'.<br>
    - Analyzes and visualizes data using KDE plot and box plots.<br>
    - Replaces categorical values with numerical values.<br>
    - Saves the processed data to 'train_data.csv'.<br>
    - Saves label encoder instances for future use.<br>



-------------------------------------2. Model Development ('2. bigmart_modeldev.ipynb')-------------------------------------<br>
    - Imports necessary libraries.<br>
    - Reads the processed training data.<br>
    - Splits the data into features (X) and the target variable (y).<br>
    - Applies various regression models: Linear Regression, Ridge Regression, Lasso Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost, 	LightGBM, and CatBoost.<br>
    - Conducts hyperparameter tuning using GridSearchCV for Gradient Boosting.<br>
    - Saves the best model using joblib.<br>
    - Evaluates and prints the RMSE for each model.<br>
    - Extracts feature importance from the Gradient Boosting model.<br>
    - Prints and visualizes feature importance.<br>



-------------------------------------3. Test Data Processing ('3. bigmart_testdatacleaning.ipynb')-------------------------------------<br>
    - Reads the test data ('test.csv').<br>
    - Applies the same data preprocessing steps as the training data.<br>
    - Saves the processed test data to 'test_data.csv'.<br>
    - Saves label encoder instances for future use.<br>



-------------------------------------4. Sales Prediction ('4. bigmart_modeltest.ipynb)-------------------------------------<br>
    - Reads the processed test data.<br>
    - Loads the best Gradient Boosting model.<br>
    - Takes user input for a single instance and predicts the sales.<br>
    - Demonstrates how to calculate the absolute difference and percentage error between predicted and actual values.<br>
    - Applies the model to predict sales for the entire test data.<br>
    - Reverses label encoding and saves the predictions to 'test_file_with_predictions.csv'.<br>

<br>
Notes:
Please note that the code assumes the presence of the necessary data files ('train.csv' and 'test.csv'). The data files should be in the same directory as the notebooks. The processed and predicted data files ('train_data.csv' and 'test_file_with_predictions.csv') will be generated in the same directory.

<br>
Make sure to install the required libraries before running the code by executing 'pip install catboost' in your environment.
