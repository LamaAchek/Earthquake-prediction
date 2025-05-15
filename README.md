Earthquake Prediction with XGBoost
This project implements a machine learning pipeline designed to predict earthquake occurrences using historical seismic data. The objective is to classify whether an earthquake exceeding a specific magnitude threshold (e.g., 2.5) will occur within the next seven days. The model leverages engineered features such as rolling statistics, exponential moving averages, and historical patterns to inform predictions.

Project Features
Model: XGBoost Classifier with performance evaluated using AUC (Area Under the Curve)

Temporal Feature Engineering:

Rolling statistics (mean and count) with window sizes of 3, 7, and 14 days

Exponential Weighted Moving Averages (EWMA) of seismic attributes

Database Integration: Utilizes SQLite to store processed features and prediction outputs

Evaluation Metrics:

AUC score

ROC curve visualization for model performance assessment

Prediction View:

Geographic display of predicted earthquake events based on latitude and longitude

Problem Framing: Binary classification for earthquake events, with a configurable magnitude threshold (default: 2.5)

System Requirements
Python 3.7 or higher

Required Python packages:

pandas

numpy

xgboost

sqlalchemy

matplotlib

sqlite3 (built-in with Python)

To install all dependencies, run:
pip install pandas numpy xgboost sqlalchemy matplotlib
