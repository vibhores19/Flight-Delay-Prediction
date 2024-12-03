
# Flight Delay Prediction

## Overview

This project predicts flight delays using historical flight data from 2013 to 2018. The goal is to evaluate different machine learning models and compare their performance across two computational environments:
1. **On-Premises Execution:** Training and evaluation performed on a local computer.
2. **AWS SageMaker:** Cloud-based training and evaluation.

The project leverages three machine learning models:
- **Logistic Regression**
- **Linear Regression**
- **XGBoost**

Through this analysis, we provide insights into the factors contributing to flight delays, as well as a comparative study of execution time, accuracy, and scalability between on-premises and cloud-based solutions.

---

## Features of the Project
- **Data Extraction:** Monthly flight data from 2013 to 2018 is extracted from a zip file containing CSV files for each month.
- **Data Preprocessing:** 
  - Handling missing values, outliers, and irrelevant features.
  - Feature engineering for time, geographic, and delay-specific variables.
- **Model Training and Evaluation:**
  - Logistic Regression, Linear Regression, and XGBoost models are trained.
  - Performance metrics (e.g., accuracy, precision, recall) are calculated.
- **Comparative Analysis:** Results are compared for both local (on-premises) and cloud-based (AWS SageMaker) environments.

---

## Dataset

### Source:
- Historical flight data containing details of over five years of flight schedules and delays.

### Features:
The dataset contains the following key columns:
- **Time Features**: `Quarter`, `Month`, `DayofMonth`, `DayOfWeek`, `CRSDepTime`, `CRSArrTime`.
- **Flight Information**: `FlightDate`, `Reporting_Airline`, `Tail_Number`, `Flight_Number_Reporting_Airline`.
- **Geographical Features**: `Origin`, `Dest`, `OriginCityName`, `DestCityName`, `Distance`.
- **Delay Indicators**:
  - `DepDelay`, `DepDelayMinutes`, `DepDel15` (departure delay over 15 minutes).
  - `ArrDelay`, `ArrDelayMinutes`, `ArrDel15` (arrival delay over 15 minutes).
- **Other Features**: Taxi times (`TaxiOut`, `TaxiIn`), reasons for delay (`CarrierDelay`, `WeatherDelay`, etc.).

### Target Variable:
- **Departure Delay (`DepDel15`)**: Binary variable indicating whether a flight was delayed by 15 minutes or more.

---

## Installation and Setup

### Prerequisites:
- **Python** (Version 3.8 or higher)
- Libraries:
  - `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`, `seaborn`

### Steps to Run Locally:
1. Clone the repository:
   ```bash
   git clone https://github.com/vibhores19/Flight-Delay-Prediction.git
   cd Flight-Delay-Prediction
