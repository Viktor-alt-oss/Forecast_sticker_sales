# Forecasting Sticker Sales - Kaggle Playground Series 2025

## Project Overview
**Project Name:** Forecasting Sticker Sales for Kaggle-branded Products  
**Competition:** Kaggle Playground Series - January 2025  
**Goal:** Predict multiple years worth of sales for various Kaggle-branded stickers across different countries and stores  

## Project Description
This project is part of the 2025 Kaggle Playground Series, which provides approachable datasets for practicing machine learning skills. The challenge focuses on time series forecasting of sticker sales across different countries and stores.

## Project Objectives
- Develop an accurate forecasting model for Kaggle-branded sticker sales  
- Handle time series data with multiple seasonal patterns  
- Incorporate country, store, and product features into the model  
- Address non-stationarity in the sales data  
- Create a robust pipeline for preprocessing and prediction  

## Dataset Description
The dataset contains synthetic sales data for Kaggle-branded stickers with the following characteristics:  

**Time period:** Multiple years of daily sales data  

**Features:**  
- Date  
- Country (Canada, Finland, Italy, Kenya, Norway, Singapore)  
- Store type (Discount Stickers, Premium Sticker Mart, Stickers for Less)  
- Product type (Holographic Goose, Kaggle, Kaggle Tiers, Kerneler, Kerneler Dark Mode)  
- Number of units sold (target variable)  

**Data characteristics:**  
- Weekend and holiday effects  
- Seasonality patterns  
- Country-specific variations  
- Product popularity trends  

## Solution Approach

### Data Exploration and Preprocessing
- Performed time series decomposition to identify trends and seasonality  
- Conducted Augmented Dickey-Fuller test to check stationarity  
- Handled missing values by imputing with product-wise mean sales  
- Created temporal features (day, month, year, day of week)  
- Added cyclical features using sine/cosine transformations  
- Implemented one-hot encoding for categorical variables  

### Modeling
Evaluated multiple models using time-series cross-validation:  
- Linear Regression (baseline)  
- Decision Tree Regressor  
- Support Vector Regression  

**Pipeline components:**  
- Custom feature generation  
- Mean imputation  
- Standard scaling  
- Linear Regression (final model)  

## Results
- Achieved a **Mean Absolute Percentage Error (MAPE) of 0.625** on the test set  
- The model captures both seasonal patterns and product-specific trends  
- Implemented a production-ready pipeline for making predictions  

## How to Use
1. Clone the repository  
2. Install required dependencies (`pandas`, `numpy`, `scikit-learn`, `statsmodels`, `matplotlib`)  
3. Run the Jupyter notebook to reproduce the analysis  
4. Use the trained pipeline (`Forecasting_Sticker_Sales.joblib`) for new predictions  

## Files
- `train_forecast_sticker_sales.csv`: Training data  
- `test_forecast_sticker_sales.csv`: Test data for predictions  
- `sample_submission.csv`: Example submission format  
- `Forecasting_Sticker_Sales.joblib`: Trained model pipeline  
- `Forecasting_Sticker_Sales.csv`: Final predictions  

## Future Improvements
- Incorporate holiday calendar information  
- Add economic indicators as external features  
- Experiment with more complex models (XGBoost, LSTM)  
- Implement hierarchical time series forecasting  
- Add ensemble approaches to improve accuracy  

This project demonstrates a comprehensive approach to time series forecasting with multiple seasonal patterns and categorical features, achieving competitive results while maintaining model interpretability.
