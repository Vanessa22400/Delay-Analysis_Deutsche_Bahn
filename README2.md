# Railway Delay Risk Modeling – Tübingen (Germany)
Data-driven analysis of operational reliability and critical delay prediction using one year of Deutsche Bahn data.

---

## 📌 Business Context

Railway delays impact commuter productivity, passenger satisfaction, and operational planning. 

Based on one full year of operational data from Tübingen Hauptbahnhof (Aug 2024 – Jul 2025), this project evaluates structural drivers of delay behavior and investigates the limits of predictability in a complex railway network.

---

## 🎯 Problem Statement

Can train delays be predicted using operational and temporal features?  
And if minute-level prediction is unstable, can we reliably identify high-risk delay scenarios?

---

## 🧭 Objectives

- Identify structural delay patterns  
- Statistically validate commuter perceptions  
- Predict delay duration (regression)  
- Predict critical delays >5 minutes (classification)  
- Translate findings into actionable operational insights  

---

## 🛠 Methodology

1. Data streaming and extraction (Hugging Face public DB dataset)  
2. Exploratory Data Analysis  
3. Statistical hypothesis testing (T-tests)  
4. Feature engineering (temporal + categorical encoding)  
5. Random Forest Regression  
6. Random Forest Classification  
7. Business insight interpretation  

---

## 💻 Tools & Technologies

- Python (Pandas, NumPy)  
- Scikit-learn  
- Random Forest (Regressor & Classifier)  
- SciPy (Hypothesis Testing)  
- Statsmodels (Time-Series Decomposition)  
- Matplotlib / Seaborn  
- Folium (Geospatial Visualization)  

---

## 📊 Exploratory Highlights

![Rush Hour vs Off-Peak](images/rush_hour_comparison.png)

- Mondays show statistically significant higher delays (p ≈ 0.001).  
- Express services experience structurally higher delays than regional trains.  
- Southbound routes present stronger infrastructure bottlenecks than expected.  
- Rush hour increases both delay frequency and severity.

---

## 📈 Regression Results – Predicting Delay Duration

- MAE: 3.20 minutes  
- R²: -0.04  

Minute-level prediction proved unstable due to unobserved stochastic disruptions.

This limitation motivated a strategic pivot toward classification modeling.

---

## 🚦 Classification Results – Predicting Critical Delays (>5 min)

![Feature Importance](Images/6.Which factors are most predictive of a Critical Delay?.png
)


- Accuracy: 82%  
- Precision (On-Time): 0.86  
- Recall (Critical Delay): 0.27  

While extreme delays remain partially unpredictable, the model provides a reliable “on-time” signal and supports risk-based decision frameworks.

---

## 🔎 Key Insights

- **Monday Effect confirmed statistically**  
- **Seasonality is a stronger predictor than hour of departure**  
- **Express services carry structural vulnerability**  
- **Passenger perception gap explained by peak-hour severity**

---

## 🚀 Business Applications

- Real-time punctuality risk alerts  
- Infrastructure bottleneck identification  
- Seasonal resource planning  
- Operational resilience analysis  

---

## 🔭 Next Steps

- Integrate weather data (DWD)  
- Merge construction logs (Baustellen)  
- Develop lightweight prediction API  
- Test Gradient Boosting models  

---

## 📌 Conclusion

This project transforms commuter perception into measurable operational insight, demonstrating both the predictive potential and structural limits of delay forecasting in complex railway systems.
