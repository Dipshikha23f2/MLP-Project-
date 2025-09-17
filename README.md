**Engage2Value: From Clicks to Conversions 🎯**

Predict purchase value from multi-session digital behavior using Machine Learning.

This project is based on the Engage-2 Value: From Clicks to Conversions Kaggle competition. The challenge focuses on analyzing customer session-level data and building predictive models that estimate the purchaseValue during a given session.

📌 Problem Statement

The dataset captures detailed session-level information from a large-scale digital commerce platform. Each row corresponds to a unique user session and contains:

User Behavior & Session Metrics: totalHits, pageViews, bounces, new_visits, sessionNumber, sessionStart.

Device & Technical Attributes: deviceType, OS, browser, screenSize, language, browserMajor, etc.

Traffic & Marketing Source: userChannel, trafficSource.medium, campaign, ad click info, referral path.

Geographical Context: city, country, region, continent, metro, geoCluster.

Identifiers: userId, sessionId.

🎯 Target Variable:

purchaseValue → The total amount spent during the session (numeric regression target).

📂 Dataset

train_data.csv – Training dataset

test_data.csv – Test dataset (for predictions)

sample_submission.csv – Submission template


🛠️ Tech Stack

Python 3

NumPy, Pandas → Data preprocessing & manipulation

Matplotlib, Seaborn → Visualization & EDA

Scikit-learn → Pipelines, preprocessing, modeling, evaluation

XGBoost, LightGBM, RandomForest → Regression models

SciPy → Statistical analysis

🚀 Workflow

Data Import & Exploration

Loaded training & test datasets.

Inspected structure, data types, and target distribution.

Data Cleaning & EDA

Removed outliers (extreme purchase values).

Analyzed distributions, correlations, and categorical impacts.

Feature Engineering

Extracted time-based features from sessionStart.

Processed device/browser strings into categorical variables.

Encoded categorical features (OneHotEncoder).

Scaled skewed numeric features.

Modeling

Trained multiple models:

RandomForestRegressor 🌲

XGBRegressor ⚡

LGBMRegressor 💡

Built a Residual-Corrected Model for improved predictions.

Applied RandomizedSearchCV for hyperparameter optimization.

Evaluation

Metric: R² Score, MAE, RMSE.

📊 Results
Model	R² Score	MAE (Millions)	RMSE (Millions)
Random Forest 🌲	 0.936	 7.69	   50.55
XGBoost ⚡	       0.891	 18.80	 64.94
LightGBM 💡      	 0.631	 23.55	 128.47
Residual-based Model 🏆	⭐ Highest	⚡ Lowest overall	🏆 Best fit

✅ Best Model → Residual-based RandomForest approach

Achieved highest R² score

Lowest overall MAE & RMSE

Most reliable fit for predicting purchaseValue


🙌 Acknowledgements

Competition: Engage-2 Value: (https://www.kaggle.com/competitions/engage-2-value-from-clicks-to-conversions/data?select=sample_submission.csv)

Dataset provided under Kaggle competition rules.

🔗 Author: Dipshikha
🎓 Diploma in Data Science, IIT Madras
💡 Passionate about Data Science, ML Engineering, and AI-driven business solutions.
