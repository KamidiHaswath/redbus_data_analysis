Red Bus Seat Count Prediction Analysis
Project Overview
This is a machine learning project focused on predicting bus seat occupancy for RedBus, a popular online bus booking platform. The goal is to forecast the final seat count for specific bus routes on given dates.
Dataset Structure
The analysis works with three main datasets:

Train Dataset (67,200 records)

Contains route information with date of journey (doj), source ID (srcid), and destination ID (destid)
Includes target variable: final seat count for each route


Test Dataset (5,900 records)

Similar structure to training data but without the target variable
Used for generating predictions for submission


Transactions Dataset (2,266,100 records)

Detailed transaction-level data with bus information
Contains features like bus type, fare, seat capacity, ratings, and actual seat bookings



Key Features & Methodology
Feature Engineering:

Time-based features: day of week, month, weekend indicators
Route aggregations: average seat counts, trip frequency, fare statistics
Bus characteristics: ratings, seat capacity, bus types

Machine Learning Approach:

Algorithm: LightGBM (Light Gradient Boosting Machine)
Handles missing values and categorical variables effectively
Provides feature importance rankings for interpretability

Model Performance:

Validation RMSE: ~479.5 (Root Mean Square Error)
Uses train-validation split for model evaluation

Business Applications
This analysis can help RedBus with:

Dynamic Pricing: Adjust prices based on predicted demand
Route Planning: Optimize bus schedules for high-demand routes
Inventory Management: Better allocation of bus capacity
Revenue Optimization: Maximize seat utilization across different routes

Technical Implementation

Built using Python with pandas, scikit-learn, and LightGBM
Jupyter notebook environment for iterative development
Automated feature engineering and model training pipeline
Generates CSV submission file for predictions

This type of demand forecasting is crucial for transportation companies to optimize operations and improve customer experience while maximizing revenue.
