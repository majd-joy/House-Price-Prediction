🏠 California Housing Prices Prediction
📌 Project Overview

This project analyzes the California Housing Prices dataset (from Kaggle) and builds a predictive model for estimating median house values using Linear Regression (OLS).

The dataset contains census data from California, including geographic coordinates, property characteristics, and demographic information. Our goal was to preprocess the data, engineer features, and evaluate model performance.

📂 Dataset Source: Kaggle – California Housing Prices

Size: 20,640 entries (20,433 valid for total_bedrooms)

Features:

Geographic: Longitude, Latitude

Property: Housing Median Age, Total Rooms, Total Bedrooms

Demographics: Population, Households, Median Income

Categorical: Ocean Proximity (e.g., NEAR BAY, INLAND, NEAR OCEAN)

Target Variable: Median House Value (in USD)

⚙️ Data Preprocessing

Handling Missing Values

total_bedrooms had 207 missing values → filled using median imputation.

Outlier Treatment

Applied IQR method to detect and replace outliers with median values.

Feature Scaling

Standardized all numerical features using Z-score normalization.

Categorical Encoding

Converted ocean_proximity into numerical labels.

Feature Engineering

Created avg_rooms_per_household = total_rooms / households.

Dropped highly correlated features (total_rooms, households) to reduce multicollinearity.

📊 Data Insights

Median Income shows the strongest correlation with housing prices.

Geographic features (latitude, longitude) revealed non-linear spatial patterns.

Room/Household features benefited from transformations.

Significant right skew observed in rooms, bedrooms, and population counts.

🧮 Model Development

Algorithm: Ordinary Least Squares (Linear Regression)

Model Assumptions Tested:

✅ Linearity (partially satisfied)

⚠️ Multicollinearity (resolved with feature engineering)

⚠️ Residual Normality (violations due to capped house values at $500,001)

Key Findings:

R² Score: 0.598 → Model explains ~60% of variance in housing prices.

Interpretation: Moderate explanatory power (typical for real estate models).

📈 Results

Median Income contributes +$56,338 per unit to housing value.

Longitude & Latitude negatively influence housing values (regional effects).

Bedrooms add value, while higher population density reduces it.

👩‍💻 Contributors

Majd Bdour 

Furat Al-Jarrah 

✅ Future Work

Experiment with non-linear models (Random Forest, XGBoost).

Apply regularization techniques (Lasso, Ridge) to improve stability.

Incorporate geospatial modeling for location-based effects.
