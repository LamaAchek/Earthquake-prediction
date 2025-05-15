# Earthquake Prediction with XGBoost

This project builds a machine learning pipeline to predict earthquake occurrences using historical seismic data. The goal is to classify whether an earthquake above a certain magnitude (e.g., 2.5) will occur within a 7-day horizon using features like rolling statistics, exponential moving averages, and past patterns.

---

## 🚀 Features

- 🧠 Model: XGBoost Classifier (with AUC evaluation)
- 🕒 Temporal Feature Engineering:
  - Rolling mean & count (window sizes: 3, 7, 14)
  - Exponential Weighted Moving Averages (EWMA)
- 🗂 SQLite Database integration for storing features and predictions
- 📊 ROC Curve plotting and AUC evaluation
- 📍 Live prediction view with latitude/longitude for visualization or mapping
- 🧪 Binary classification of events with adjustable magnitude threshold

---

## 🧰 Requirements

- Python 3.7+
- pandas
- numpy
- xgboost
- sqlalchemy
- matplotlib
- sqlite3

Install all dependencies:
```bash
pip install pandas numpy xgboost sqlalchemy matplotlib
