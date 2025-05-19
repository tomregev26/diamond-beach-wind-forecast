
Wind Prediction using Random Forest
This project focuses on predicting wind conditions at the Diamond Beach (Kinneret) using historical meteorological data collected from various weather stations across Israel. The selected machine learning algorithm is Random Forest, chosen due to its high prediction accuracy and its interpretable structure, which allows users to visualize decision trees and understand the logic behind predictions.

Project Structure
The repository includes the following directories:

data/drop/: Yearly CSV files containing raw weather station data from 2000 onwards.

notebooks/: Jupyter notebooks detailing each step of the project, including data cleaning, feature engineering, normalization, model training, and evaluation.

output/: Contains prediction results and any generated plots.

model/ (optional): Folder for storing saved model artifacts.

Algorithm
The Random Forest algorithm was selected because it offers the following advantages:

High accuracy, especially in regression and classification tasks involving structured data.

Robustness to missing values and feature scaling.

The ability to measure feature importance and visualize decision paths through individual trees.

Data Description
Each CSV file in the data/drop/ directory contains hourly meteorological observations from one or more weather stations. The data includes the following columns:

Station: Name of the weather station.

Date & Time (Summer): Timestamp of the recorded observation.

Pressure at station level (hPa): Atmospheric pressure measured at the station.

Global radiation (W/m^2): Solar radiation intensity.

Relative humidity (%): Relative humidity level.

Temperature (°C): Ambient temperature.

Wind direction (°): Wind direction in degrees.

Gust wind direction (°): Direction of gust wind in degrees.

Wind speed (kt): Wind speed in knots.

Gust wind speed (kt): Gust wind speed in knots.

Processing Workflow
Preprocessing (01_preprocessing.ipynb)
Handles missing values and formats the raw data.

Normalization (03_normalize.ipynb)
Applies feature scaling where necessary.

Model Training (07_model.ipynb)
Trains a Random Forest model on historical wind data.

Model Evaluation (08_test.ipynb)
Tests the model on unseen data and visualizes accuracy and error trends.

Model Output
The trained model outputs wind condition predictions for the Diamond Beach area. Results include:

Predicted wind speed and gust values.

Accuracy metrics and error analysis.

Feature importance rankings.

Optional visualizations of selected decision trees.

Summary
Random Forest was found to be the most effective algorithm for this project due to its strong performance and interpretability. The data pipeline includes all necessary steps for cleaning, transforming, modeling, and evaluating wind-related predictions based on long-term historical data.
