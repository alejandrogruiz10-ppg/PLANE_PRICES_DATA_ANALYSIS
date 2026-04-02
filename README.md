Aircraft Price Analysis
Overview

This project analyzes aircraft data to identify the key factors that drive pricing across different aircraft categories. The analysis focuses on understanding how structural characteristics and performance metrics influence aircraft value.

The project combines data cleaning, feature engineering, exploratory data analysis, and machine learning to generate insights and build a predictive model.

Business Context

The aircraft market includes a wide range of models, from small piston aircraft to high-performance jet aircraft, each with significantly different characteristics and pricing structures.

Understanding what drives aircraft pricing is critical for manufacturers, buyers, and investors, as it allows better valuation, comparison, and decision-making.

Aircraft price is influenced by multiple factors, including size, engine power, performance, and operational capabilities. However, these relationships are not always linear and may vary across different aircraft categories.

Objective
Identify the main factors influencing aircraft prices
Analyze how size and performance affect pricing
Detect whether the dataset contains distinct aircraft segments
Evaluate whether efficiency plays a more important role than size alone
Build a predictive model for aircraft prices
Dataset

The dataset contains aircraft specifications and pricing information, including:

Engine type
Engine power
Aircraft dimensions
Fuel capacity
Weight
Range
Price
Data Cleaning
Converted numerical columns stored as text into numeric format
Standardized categorical variables (uppercase and trimmed text)
Transformed aircraft dimensions from "ft/in" format into numeric values in feet
Handled missing values using median imputation
Feature Engineering

New variables were created to better capture aircraft characteristics:

Aircraft Size: length × wingspan
Power to Size Ratio: engine power relative to aircraft size
Weight to Size Ratio: structural density

These features provide a more meaningful representation of aircraft performance and structure.

Outlier Analysis

Approximately 15% of the observations were initially detected as outliers.

However, these values represent structurally different aircraft types (primarily jet aircraft) rather than errors. This indicates that the dataset is not homogeneous and contains distinct segments.

Exploratory Data Analysis
Key Findings
Aircraft prices are right-skewed, with most observations in lower price ranges
Jet and propjet aircraft are significantly more expensive than piston aircraft
Aircraft size has a strong positive relationship with price
Engine power is positively associated with price
Performance efficiency (power-to-size ratio) shows a stronger relationship with price than size alone
The dataset contains distinct aircraft segments, requiring segmented analysis
Modeling

A machine learning model (XGBoost Regressor) was used to predict aircraft prices.

Train-test split: 80/20
Model type: Gradient boosting (XGBoost)
Objective: Predict continuous price values
Model Performance
R²: ~0.88
MAE: ~236,000

The model explains approximately 88% of the variance in aircraft prices, indicating strong predictive performance.

On average, prediction errors are within an acceptable range, making the model suitable for approximate valuation and comparison.

Key Insights
Aircraft pricing is driven by both structural size and performance characteristics
Efficiency metrics (power-to-size and weight-to-size) are stronger predictors than raw variables
Aircraft pricing follows an efficiency-driven model rather than a purely size-based model
The presence of multiple aircraft categories highlights the importance of segmentation
Conclusion

Aircraft pricing is primarily driven by performance efficiency rather than size alone.

While larger aircraft tend to have higher prices, the strongest predictors are derived efficiency metrics such as power-to-size and weight-to-size ratios.

Additionally, the presence of distinct aircraft categories highlights the importance of segmentation, suggesting that pricing models should account for structural differences between aircraft types.

Technologies Used
Python
pandas
numpy
matplotlib
seaborn
xgboost
scikit-learn
Project Structure
PLANE_PRICES_DATA_ANALYSIS.ipynb
Plane_Price.csv
Author

José Alejandro Gutiérrez Ruiz
