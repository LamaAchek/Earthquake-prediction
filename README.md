# Earthquake Prediction with XGBoost

This project implements a machine learning pipeline to predict earthquake events using historical seismic data. 

The primary objective is to classify whether an earthquake exceeding a configurable magnitude threshold (e.g., 2.5) will occur within the next **7-day window**. 

The model leverages:
- **Rolling statistics** (mean and count)
- **Exponential Weighted Moving Averages (EWMA)**
- **Temporal seismic patterns**

These engineered features help identify early signals of seismic activity and improve the accuracy of earthquake prediction.

## 1. Key Features

### Model
- **XGBoost Classifier**
- Evaluated using:
  - AUC (Area Under the Curve)
  - ROC Curve metrics

### Temporal Feature Engineering
- Rolling statistics (mean and count) with window sizes of 3, 7, and 14 days
- Exponential Weighted Moving Averages (EWMA) for key seismic indicators

### Database Integration
Uses **SQLite** to store:
- Engineered features
- Model predictions
- Evaluation results

### Prediction View
- Displays geographic coordinates (latitude, longitude) of predicted events
- Can be visualized on a map interface or integrated with real-time dashboards

### Classification Approach
- Binary classification:
  - `1` → Earthquake ≥ 2.5 magnitude
  - `0` → No significant earthquake
- Magnitude threshold is configurable

---

## 2. System Requirements

### Software Dependencies
- Python 3.7+
- `pandas`
- `numpy`
- `xgboost`
- `sqlalchemy`
- `matplotlib`
- `sqlite3` (built-in with Python)

### Installation
Install all required packages using:

```bash
pip install pandas numpy xgboost sqlalchemy matplotlib
