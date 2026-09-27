# Flight-Delay-Prediction-Using-Pyspark
Scalable flight delay prediction using PySpark and machine learning on 2024 U.S. flight data with time-aware feature engineering and model evaluation.
# ✈️ Flight Delay Prediction Using PySpark & Machine Learning

A scalable machine learning project for predicting flight delays using **2024 U.S. flight data**. The project combines **PySpark-based big data processing**, time-aware feature engineering, and multiple machine learning models to identify flights likely to be delayed.

## 📌 Project Overview

Flight delays are influenced by several operational and temporal factors such as previous flight delays, airport congestion, departure time, and historical delay patterns.

This project develops an end-to-end prediction pipeline that processes large-scale flight data and predicts whether a flight will be delayed.

The workflow covers:

* Large-scale data processing using PySpark
* Data cleaning and preprocessing
* Exploratory Data Analysis
* Time-based feature engineering
* Historical delay-rate features
* Airport congestion features
* Machine learning model development
* Model comparison and evaluation
* Threshold tuning for classification

## 🎯 Objectives

* Predict whether a flight will be delayed.
* Process large-scale flight data efficiently using PySpark.
* Engineer meaningful temporal and historical features.
* Compare different classification algorithms.
* Evaluate model performance using appropriate classification metrics.
* Build a leakage-safe prediction pipeline using chronological data splitting.

## 📊 Dataset

The project uses **2024 U.S. flight data** containing flight-level operational and schedule information.

The dataset includes information related to:

* Flight date
* Airline
* Origin and destination airports
* Scheduled departure and arrival times
* Actual departure and arrival information
* Departure delay
* Arrival delay
* Flight distance
* Cancellation information
* Other operational attributes

## 🛠️ Technologies Used

* **Python**
* **PySpark**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **XGBoost**
* **Jupyter Notebook**

## 🔄 Project Workflow

```text
Raw Flight Data
       ↓
Data Cleaning & Preprocessing
       ↓
Exploratory Data Analysis
       ↓
Time-Based Feature Engineering
       ↓
Historical Delay Features
       ↓
Airport Congestion Features
       ↓
Chronological Train / Validation / Test Split
       ↓
Model Training
       ↓
Model Comparison
       ↓
Threshold Tuning
       ↓
Final Test Evaluation
```

## ⚙️ Feature Engineering

Several features were developed to capture historical and operational patterns in flight delays.

### Historical Delay Features

Historical delay information was calculated using previous flight observations while maintaining chronological ordering.

These features help the model capture patterns such as:

* Previous flight delays
* Historical airport delay rates
* Historical airline delay rates
* Time-based delay patterns

### Airport Congestion Features

Features related to airport activity and congestion were engineered to capture operational conditions that may contribute to delays.

### Time-Based Features

Temporal information was extracted from flight schedules to capture patterns related to:

* Hour of departure
* Day of week
* Month
* Other time-dependent patterns

## 🤖 Machine Learning Models

The following classification models were evaluated:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. XGBoost

The models were compared using classification metrics rather than relying only on accuracy.

## 📈 Model Evaluation

The final evaluation was performed on an unseen chronological test set.

Key evaluation metrics include:

* F1-Score
* ROC-AUC
* Precision
* Recall
* Confusion Matrix

### Final Test Performance

| Metric   | Score |
| -------- | ----: |
| F1-Score | 0.327 |
| ROC-AUC  | 0.601 |

The relatively low F1-score reflects the difficulty of predicting flight delays, particularly when the delayed class is less frequent and operational factors are highly variable.

## 🔐 Preventing Data Leakage

A major focus of the project was maintaining chronological integrity.

Instead of randomly splitting the observations, the project uses **time-based train, validation, and test splits**.

Historical features were also constructed using information available prior to the flight being predicted.

This prevents future information from being unintentionally used during model training.

## 💡 Key Takeaways

* Flight delay prediction is a challenging classification problem with substantial variability.
* Historical delay patterns provide useful predictive information.
* Airport-level operational patterns can help capture congestion-related effects.
* Time-aware validation is important for real-world forecasting problems.
* F1-score and ROC-AUC provide more informative evaluation than accuracy alone for this problem.
* PySpark provides a scalable framework for processing large flight datasets.



## 👩‍💻 Author

**Atchaya A D R**

B.E. (Hons) Electronics and Communication Engineering
Data Science / Machine Learning / AI


