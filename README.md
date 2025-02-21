# House_price_Advance
This project aims to predict house prices using machine learning techniques. The dataset contains various features related to houses, such as their size, quality, location, and other attributes. The goal is to build an accurate predictive model that can estimate the sale price of a house based on these features.
The project includes data preprocessing, feature engineering, exploratory data analysis (EDA), and training a regression model using XGBoost.

Dataset
The dataset used in this project consists of two files:

train.csv : Contains the training data with features and target variable (SalePrice).
test.csv : Contains the test data without the target variable.
sample_submission.csv : A sample submission file for predictions.
Key characteristics of the dataset:

Numerical and categorical features.
Missing values in some columns.
Features related to house properties (e.g., area, condition, materials).
Preprocessing
Steps Performed:
Handling Missing Values :
Columns with more than 50% missing values were dropped.
Remaining missing values were filled using median (for numerical features) or mode (for categorical features).
Encoding Categorical Variables :
Label encoding was applied to ordinal categorical variables.
One-hot encoding was applied to nominal categorical variables.
Outlier Detection and Removal :
Outliers were detected using the Interquartile Range (IQR) method.
Outliers were removed from numerical columns where necessary.
Log Transformation :
Applied log transformation to numeric features to reduce skewness and improve model performance.
Dropping Irrelevant Features :
Removed features with low variance or high correlation with other features.
Feature Engineering
New features were created to enhance the predictive power of the model:

Total Floors : Sum of 1stFlrSF and 2ndFlrSF.
House Quality Score : Product of OverallCond and OverallQual.
Total Bathrooms : Combined counts of full and half bathrooms in the basement and main floors.
Irrelevant or redundant features were dropped after creating new ones.

Modeling
Model Used:
XGBoost Regressor : A gradient boosting algorithm well-suited for regression tasks.
Training Process:
Split the dataset into training and testing sets (80% train, 20% test).
Trained the XGBoost model on the training set.
Evaluated the model using Root Mean Squared Error (RMSE) on the test set.
Results:
Validation RMSE: ~27,173.7334
This value indicates reasonable performance, but there is room for improvement.
Results
The model achieved a validation RMSE of approximately 27,173.7334 , which corresponds to about 15.1% of the mean target value (SalePrice). While this result is acceptable, further optimization could improve accuracy.
