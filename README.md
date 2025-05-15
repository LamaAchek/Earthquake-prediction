Earthquake Prediction with XGBoost
________________________________________
Overview
This project implements a machine learning pipeline to predict earthquake events using historical seismic data. The goal is to classify whether an earthquake above a configurable magnitude threshold (e.g., 2.5) will occur within the next 7 days.
Using a combination of rolling statistics, exponential weighted moving averages (EWMA), and past patterns, the model identifies early signals of seismic activity.
________________________________________
1. Key Features
 Model
•	XGBoost Classifier
•	Evaluated using AUC (Area Under the Curve) and ROC Curve metrics
Temporal Feature Engineering
•	Rolling statistics (mean and count) with window sizes of 3, 7, and 14 days
•	Exponential Weighted Moving Averages (EWMA) for key seismic indicators
Database Integration
•	Uses SQLite to store:
o	Engineered features
o	Model predictions
o	Evaluation results
 Prediction View
•	Displays geographic coordinates (latitude, longitude) of predicted events
•	Can be visualized on a map interface or integrated with real-time dashboards
 Classification Approach
•	Binary classification:
o	1 → Earthquake ≥ 2.5 magnitude
o	0 → No significant earthquake
•	Magnitude threshold is configurable
________________________________________
2. System Requirements
Software Dependencies
•	Python 3.7+
•	pandas
•	numpy
•	xgboost
•	sqlalchemy
•	matplotlib
•	sqlite3 (built-in with Python)
 Installation
Use the following command to install all required packages:
pip install pandas numpy xgboost sqlalchemy matplotlib
________________________________________
3. Applications and Use Cases
•	Early earthquake alert systems
•	Disaster preparedness platforms
•	Integration with geospatial dashboards
•	Academic and government research on seismic trends

