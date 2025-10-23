This project is a full-stack web application that predicts transportation costs and budget risks for logistics operations. It uses a machine learning backend (built with Python, Flask, and Scikit-learn) to analyze trip data and a dynamic frontend (built with HTML, Tailwind CSS, and JavaScript) to provide real-time forecasts to a user.

✨ Features

Accountant's Estimate: Predicts the exact fuel cost of a trip with high accuracy (MAE < ₹10) using a Random Forest Regressor.

Risk Manager's Warning: Provides a qualitative risk assessment (Low, Medium, High, Critical) of the trip going over budget, using a Random Forest Classifier.

Dynamic Data Fetching: The user only enters the trip date; the backend automatically fetches:

Historical fuel prices from a pre-scraped CSV.

Real-time weather forecasts from the Open-Meteo API.

Beautiful UI: A responsive, glassmorphism-style UI built with Tailwind CSS, featuring a dynamic results dashboard.

Output of the following Project: 
<img width="2880" height="1556" alt="image" src="https://github.com/user-attachments/assets/64e7e5b9-222c-4f77-86bc-1b8974ce4a9d" />

