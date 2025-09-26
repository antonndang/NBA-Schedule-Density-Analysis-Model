# NBA Schedule Density Analysis

Analyze the **2024–25 NBA schedule** to quantify **game density, travel load, and fatigue factors**.  
This notebook computes and visualizes **home/away splits**, **back-to-backs (B2B)**, and **4-in-6** stretches, and produces **comparative workload** views across teams.

## Features
- **Schedule parsing & cleaning** → convert raw schedule into a tidy DataFrame (date, opponent, home/away, location).
- **Fatigue metrics** → flags for **B2B**, **4-in-6**, and other dense stretches.
- **Visualizations** → per-team calendars/timelines highlighting **home/away**, **B2B**, and **4-in-6** sequences.
- **Comparative analysis** → counts and summaries to compare workload across teams.

## Tech Stack
- **Feature Engineering:** rolling game density, days since last game, B2B/4-in-6 indicators, cumulative travel miles, time-zone changes.
- **Models:** Logistic Regression, Random Forest, XGBoost/LightGBM (win probability / fatigue impact), K-Means or DBSCAN (cluster “stress” segments), Isolation Forest (anomaly stretches), ARIMA/Prophet (time-series fatigue trends).
- **Evaluation:** Accuracy, ROC-AUC (classification), LogLoss; MAE/RMSE (regression); cross-validation; SHAP/feature importance.
- **Libraries:** scikit-learn, XGBoost, LightGBM, statsmodels/Prophet, NumPy, Pandas.
