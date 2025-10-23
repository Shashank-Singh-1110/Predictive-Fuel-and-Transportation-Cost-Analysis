🤖 Model Building

Two models are trained and saved using scikit-learn and joblib.

Model 1: Cost Prediction (The "Accountant")

Model: RandomForestRegressor (random_forest_cost_model.pkl)

Purpose: To predict the exact, continuous Total_Fuel_Cost.

Reason: A Random Forest was chosen over a simple Linear Regression because it can capture the complex, non-linear relationships between load, distance, weather, and cost, resulting in a much higher R² (0.99+) and a very low Mean Absolute Error (MAE) of ~₹7-8.

Model 2: Risk Analysis (The "Risk Manager")

Model: RandomForestClassifier (random_forest_risk_model.pkl)

Purpose: To predict a binary class: will this trip go over budget? (Yes/No).

Reason: We initially used LogisticRegression but found it was poorly calibrated, often predicting 100% risk for trips that were safely under budget. A RandomForestClassifier provides more nuanced and reliable probabilities, which we convert into a qualitative "Risk Level" (Low, Medium, High, Critical) in the frontend.
