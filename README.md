# ✈️ Flight Cancellation Prediction using Azure Machine Learning Designer

## 📜 Project Overview

This project aims to predict **flight cancellations** using machine learning techniques within **Azure Machine Learning Designer**. The analysis focuses on key flight-related features to build a predictive model that identifies the likelihood of a flight being canceled.

## 📊 Dataset

The dataset used for this analysis includes various features related to flight operations, such as departure and arrival times, delays, distances, and more. The primary target variable for prediction is **`CANCELLED`**, which indicates whether a flight was canceled.

### 🗂️ Selected Columns for Analysis

- **FL_DATE**: The date of the flight.
- **AIRLINE**: The airline operating the flight.
- **FL_NUMBER**: The flight number.
- **ORIGIN**: The origin airport code.
- **DEST**: The destination airport code.
- **CRS_DEP_TIME**: Scheduled departure time.
- **DEP_TIME**: Actual departure time.
- **DEP_DELAY**: Departure delay in minutes.
- **TAXI_OUT**: Taxi-out time in minutes.
- **WHEELS_OFF**: Time when wheels are off the ground.
- **WHEELS_ON**: Time when wheels touch down.
- **TAXI_IN**: Taxi-in time in minutes.
- **CRS_ARR_TIME**: Scheduled arrival time.
- **ARR_TIME**: Actual arrival time.
- **ARR_DELAY**: Arrival delay in minutes.
- **CANCELLED**: Cancellation indicator (**Target Variable**).
- **DIVERTED**: Diverted flight indicator.
- **DISTANCE**: Distance between origin and destination.
- **CRS_ELAPSED_TIME**: Scheduled elapsed time.
- **ELAPSED_TIME**: Actual elapsed time.
- **AIR_TIME**: Time spent in the air.

## 🔄 Handling Missing Values

Missing values were handled using the following strategies:
- Columns with **less than 5%** missing values were imputed using the **mean** value.
- Columns with **high percentages** of missing values were **dropped** from the analysis.

## ⚙️ Feature Engineering

Custom features were created using the following techniques:

### 🗓️ Date Transformation
- The `FL_DATE` column was transformed to extract parts such as **day of the week** and **month** to capture seasonal and weekly patterns.

### ✍️ Custom Logic
- A Python script was used to create a feature for categorizing flights as **long-haul** or **short-haul** based on the `DISTANCE` column.

## 🧠 Model Building

The following steps were followed for model building:

- **Train Model**: A **Two-Class Decision Forest** was chosen for its robustness and ability to handle imbalanced data.
- **Target Variable**: **`CANCELLED`** was set as the target variable for training the model.

## 🧪 Model Evaluation

The model was evaluated using various metrics to determine its performance in predicting flight cancellations. The results are as follows:

- **Accuracy**: 1.000
- **Precision**: 1.000
- **Recall**: 1.000
- **F1 Score**: 1.000
- **AUC**: 1.000

### 📈 Additional Insights

- The model's performance across different probability thresholds was also evaluated, showing consistent high performance across all thresholds.
- AUC scores were uniformly high, demonstrating the model's effectiveness in distinguishing between canceled and non-canceled flights.

