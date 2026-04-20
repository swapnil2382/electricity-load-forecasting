# ⚡ Electricity Load Forecasting (Machine Learning Project)

## 📌 Overview

This project predicts electricity demand using historical load and weather data.
It uses machine learning models to analyze patterns such as time, temperature, and past consumption to forecast future electricity usage.

The goal is to simulate a **real-world power demand forecasting system**.

---

## 🚀 Features

* 📊 Predict electricity demand (MW) based on input conditions
* 🧠 Uses time-series feature engineering (lags, rolling averages)
* ⚙️ Model comparison (Linear Regression, Random Forest, Gradient Boosting, XGBoost)
* 📈 Visualization of Actual vs Predicted values
* 🏆 Best model selection based on MAE
* 💾 Model saving using pickle

---

## 🧠 Machine Learning Approach

### 1. Problem Type

* Regression (predict continuous values)

### 2. Target Variable

* `nat_demand` → electricity demand (in MW)

### 3. Features Used

#### ⏱ Time-based Features

* Hour
* Day of week
* Month
* Weekend indicator
* Day of year

#### 🔁 Lag Features (VERY IMPORTANT)

* Demand 1 hour ago
* Demand 24 hours ago
* Demand 48 hours ago
* Demand 168 hours ago (same time last week)

#### 📊 Rolling Features

* 6-hour average
* 24-hour average
* 24-hour standard deviation

#### 🌡 Weather Features

* Temperature
* Humidity
* Wind speed

---

## 🤖 Models Used

| Model             | Purpose                       |
| ----------------- | ----------------------------- |
| Linear Regression | Baseline                      |
| Random Forest     | Main model (best performance) |
| Gradient Boosting | Improvement model             |
| XGBoost           | Advanced model                |

---

## 🏆 Final Model

* ✅ **Random Forest Regressor**
* 📉 MAE ≈ **19**

This model performed best on test data.

---

## 📊 Evaluation Metric

* **MAE (Mean Absolute Error)**
  Measures average prediction error.

---

## 📁 Dataset

* Electricity Load Forecasting (Panama case study)
* Contains:

  * Hourly electricity demand
  * Weather data (temperature, humidity, etc.)
  * Calendar data

---

## ⚙️ How to Run

### 1. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib xgboost kagglehub
```

### 2. Download dataset

```python
import kagglehub
path = kagglehub.dataset_download("saurabhshahane/electricity-load-forecasting")
```

### 3. Run notebook / script

* Data preprocessing
* Feature engineering
* Model training
* Evaluation

---

## 💻 Usage (Console Input Example)

User provides:

```text
Enter hour (0-23)
Enter day of week (0=Mon)
Enter month
Last hour demand
Same time yesterday demand
```

Output:

```text
Predicted demand: 591.22 MW
```

---

## 📈 Output Meaning

* The prediction represents **expected electricity demand (MW)**
* Useful for:

  * Power grid planning
  * Load balancing
  * Energy optimization

---

## 🌍 Real-world Applications

* ⚡ Power grid management
* 🏭 Industrial energy planning
* 🏙 Smart city systems
* 🔌 Demand-response systems
* 🌱 Energy efficiency optimization

---

## 🔥 Future Improvements

* 🔁 24-hour / 7-day forecasting
* ⚠️ Peak demand alerts
* 📊 Feature importance visualization
* 🌡 Real-time weather API integration
* 📉 Hyperparameter tuning
* 🌍 Multi-region forecasting

---

## 🧠 What I Learned

* Time series feature engineering
* Model comparison & evaluation
* Handling real-world datasets
* Building ML pipeline end-to-end
* Importance of lag features

---

## 👨‍💻 Author

* Your Name

---

## 📌 Note

This project is for learning and demonstration purposes but follows real-world ML practices.
