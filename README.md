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
