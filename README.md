# ✈️ **Flight Delay Prediction (Machine Learning Project)**

Predicting flight arrival delays using large-scale U.S. flight data.

---

## 📌 **Project Overview**

This project builds models to **predict arrival delays** and identify the **key factors** contributing to them.  
It includes:

* Regression (predict delay minutes)
* Classification (predict if delay > 15 min)
* Feature engineering
* SHAP model explainability
* Error analysis for operational insights

The project is optimized for clarity, performance, and real-world usability.

---

## 📂 **Dataset**

The dataset used in this project is available on Kaggle:

**Flight Delays and Cancellations**  
https://www.kaggle.com/datasets/usdot/flight-delays

(Note: The dataset is large, so it is not included in this repository.)

* **Rows:** ~5.7 million  
* **Cleaned Output:** `clean_flight_data.csv`  
* **Targets:**  
  * `ARRIVAL_DELAY` (Regression)  
  * `LATE` label (Classification, delay > 15 min)  

---

## 🔧 **Project Workflow**

1. Data loading & cleaning  
2. EDA (Exploratory Data Analysis)  
3. Feature engineering  
4. Encoding & scaling  
5. Machine learning models  
6. Model interpretation (SHAP)  
7. Error analysis (Airline, Route, Hour)  
8. Final results & conclusions  

---

## 📊 **Key Insights**

* **Departure Delay** is the strongest predictor across all models.  
* Distance, scheduled time, airline, route, and airport congestion all influence predictions.  
* Evening flights show higher unpredictability due to **delay propagation**.  
* Error patterns vary strongly by airline and route.  

---

## 🧠 **Model Performance**

### **Regression Results**

| Model                | MAE   | RMSE   | R²     |
|----------------------|-------|--------|--------|
| Linear Regression     | 8.75  | 12.53  | 0.8986 |
| Random Forest (best) | 8.74  | 12.51  | 0.8981 |
| XGBoost              | 8.01  | 14.36  | 0.8656 |

### **Classification Results (Random Forest)**

| Metric     | Score   |
|------------|---------|
| Accuracy   | 0.9351  |
| Precision  | 0.9073  |
| Recall     | 0.7131  |
| F1 Score   | 0.7986  |

---

## 🛠️ **Technologies Used**

* Python  
* Pandas, NumPy  
* Scikit-learn  
* XGBoost  
* SHAP  
* Matplotlib, Seaborn  

---

## 🚀 **Future Improvements**

* Add weather and airport congestion data  
* Try LightGBM or deep learning models  
* Deploy as an interactive dashboard (Streamlit / Power BI)  
* Real-time model serving via API  

---

## ⭐ **Summary**

This project demonstrates strong predictive performance and clear operational insights.  
The Random Forest model, supported by SHAP explanations and error analysis, provides a **reliable and interpretable system** for predicting flight delays.

---

## ✅ Key Recommendations

1. Reduce **departure delays**, as they are the strongest driver of arrival delays.  
2. Improve **airport turnaround efficiency**, especially during peak hours (15:00–21:00).  
3. Monitor **airline-wise performance** and set punctuality targets for high-delay carriers.  
4. Add additional features like **weather, airport traffic, and taxi times** to improve model accuracy.  
5. Use the model to build a **real-time delay prediction dashboard** for operational planning.  

---

## 📘 **How to Run**

### 1. Clone the repository
```bash
git clone https://github.com/abhijitchaudhari05/Flight-Delay-Prediction-using-Machine-Learning.git
cd Flight-Delay-Prediction-using-Machine-Learning
