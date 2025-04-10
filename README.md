House Prices - Advanced Regression Techniques

Competition Overview
This project is based on the Kaggle competition (https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques),
where the goal is to predict the final sale price of residential homes using a variety of regression techniques.
The challenge involves handling missing values, categorical variables, and selecting appropriate features for accurate predictions.

Our approach involves careful preprocessing of the data, extensive feature engineering, model experimentation, and hyperparameter tuning.
The final model was selected based on cross-validated RMSE performance and overall stability on unseen data.

Feature Engineering & Data Cleaning

Encoding Categorical Variables
- Used OneHotEncoder with handle_unknown='ignore'
- Integrated into a ColumnTransformer pipeline
- Applied set_output(transform='pandas') for easier integration with dataframes

Handling Missing Values
- Numerical features: SimpleImputer(strategy='median')
- Categorical features: SimpleImputer(strategy='constant', fill_value='missing')

Cleaning Strategies
- Log-transformations for skewed features
- Removal of outliers
- Standardization using StandardScaler

Feature Selection
- Pearson correlation analysis
- Model-based importance (Random Forest, Lasso)
- Recursive Feature Elimination (RFE)

Tested Models:
- Ridge
- Lasso
- RandomForestRegressor

Final Model Selection
- Chosen based on lowest cross-validated RMSE
- Stability and generalization on the test set were considered
- Final model used log-transformed target and selected features

MLflow Tracking
Experiment Tracking Link
https://dagshub.com/giorgitorro/HousePricesRegression_gtoro22.mlflow/#/experiments/1
https://dagshub.com/giorgitorro/HousePricesRegression_gtoro22.mlflow/#/experiments/2
https://dagshub.com/giorgitorro/HousePricesRegression_gtoro22.mlflow/#/experiments/3

Logged Metrics
- Training and validation RMSE
- RR Score

Final Model Results
- Best RMSE: 0.131
- Final model: Random Forest
  
