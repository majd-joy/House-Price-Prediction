# 🏠 California Housing Prices Prediction  

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/ML-scikit--learn-orange?logo=scikitlearn)
![pandas](https://img.shields.io/badge/Data-pandas-yellow?logo=pandas)
![numpy](https://img.shields.io/badge/Math-numpy-lightblue?logo=numpy)
![matplotlib](https://img.shields.io/badge/Viz-matplotlib-green?logo=plotly)

## 📌 Overview  
A Machine Learning project predicting **median house values in California** using **Linear Regression**.  
We analyzed **20,000+ census records** including location, demographics, and housing features.  

---

## 📂 Dataset  
📊 [California Housing Prices (Kaggle)](https://www.kaggle.com/)  
- 20,640 records  
- Features: `Latitude`, `Longitude`, `Median Income`, `Total Rooms`, `Ocean Proximity`  
- Target: `Median House Value` 💰  

---

## 🔧 Pipeline  

```mermaid
flowchart TD
    A[Raw Data] --> B[Preprocessing]
    B --> C[Feature Engineering]
    C --> D[Linear Regression Model]
    D --> E[Evaluation & Insights]
🧹 Missing values handled with median imputation

📉 Outliers treated using IQR method

🔢 Encoded categorical ocean_proximity

⚖️ Feature scaling via Z-score standardization

🏗️ Engineered feature: avg_rooms_per_household
📊 Results

R² = 0.598 → Model explains ~60% of housing price variance

Top predictor: Median Income (+$56k per income unit)

🌍 Geographic features show non-linear spatial effects

📈 Example Visualization:

🎥 Demo

📹 YouTube Presentation

📓 Google Colab Notebook

👩‍💻 Contributors

Majd Bdour

Furat Al-Jarrah

✨ Future Work: Try Random Forest, XGBoost, and geospatial modeling for better accuracy.
