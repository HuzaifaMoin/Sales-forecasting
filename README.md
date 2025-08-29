# Sales-forecasting
Walmart Sales Forecasting
Overview

This project focuses on forecasting weekly sales for Walmart stores using historical sales data, store information, and external factors. The goal is to build predictive models that can capture trends, seasonal effects, and economic indicators to provide accurate sales forecasts.

Dataset

The dataset consists of multiple CSV files:

train.csv – Historical weekly sales data including Store, Dept, Date, Weekly_Sales, and holiday indicators.

features.csv – Additional features such as Temperature, Fuel_Price, CPI, and Unemployment.

stores.csv – Metadata about stores, including store Type and Size.

test.csv – Test set for evaluation.

Data Preprocessing

Merged datasets (train, features, stores) into a single dataframe.

Converted Date to datetime and extracted features: Day, Month, Week, Year.

Created lag features (Lag_1 to Lag_4) to capture past sales trends.

Added rolling averages (Rolling_Mean_3, Rolling_Mean_4).

Handled missing values by dropping NaNs introduced by lag/rolling operations.

Performed one-hot encoding for categorical variables (Type, IsHoliday).

Models Used

Random Forest Regressor

Baseline ensemble model trained on extracted features.

XGBoost Regressor

Gradient boosting model with tuned parameters for better accuracy.

Evaluation Metrics

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² Score (Coefficient of Determination)

Results

Random Forest achieved a baseline performance.

XGBoost provided improved accuracy with lower RMSE and MAE, and a higher R² score.

Visualization of actual vs predicted weekly sales showed that both models captured overall trends effectively.

Visualization

The project includes plots comparing actual sales with predictions from Random Forest and XGBoost over time.

Key Learnings

Lag features and rolling averages significantly improve forecasting performance.

XGBoost outperforms Random Forest in capturing complex patterns.

External factors like CPI, fuel price, and unemployment rates impact weekly sales.

Future Work

Hyperparameter tuning for further improvement.

Incorporating deep learning models (e.g., LSTM) for time-series forecasting.

Adding more feature engineering (e.g., interaction terms, advanced seasonality decomposition).
