🧠 Early Detection of Chronic Diseases from EHRs using LSTM

This project demonstrates how to simulate electronic health record (EHR) data for multiple patient visits and use an LSTM-based deep learning model to predict the early onset of chronic diseases (e.g., diabetes, hypertension).
📁 File Structure

    synthetic_ehr.xlsx – Synthetic time-series EHR dataset (generated automatically)

    train_lstm_model.py – Python script to load the Excel file and train the LSTM model

    generate_ehr_excel.py – Python script to generate the synthetic dataset and save it to Excel

    README.md – Project overview and instructions

📦 Requirements

Install the following packages before running the code:

pip install pandas numpy scikit-learn tensorflow matplotlib openpyxl

📊 Dataset Overview

Each patient has multiple visits (time steps), with the following features:
Column	Description
patient_id	Unique identifier for each patient
timestep	Visit number (0 to 9)
age	Patient's age
bmi	Body Mass Index
bp	Blood pressure
glucose	Blood glucose level
cholesterol	Cholesterol level
activity	Physical activity level
chronic_disease	Target label (0 = No, 1 = Yes)
🚀 How to Use
1. Generate the Dataset

from generate_ehr_excel import generate_and_save_ehr_excel

generate_and_save_ehr_excel("synthetic_ehr.xlsx")

2. Train the LSTM Model

from train_lstm_model import train_lstm_from_excel

train_lstm_from_excel("synthetic_ehr.xlsx")

This will train an LSTM on the data and output accuracy metrics and plots.
📈 Sample Output

    Accuracy over training epochs

    Final test accuracy (e.g., 85–90%)

    ROC curve (optional extension)

✅ Features

    Synthetic EHR generator with time-series records

    End-to-end LSTM pipeline using TensorFlow/Keras

    Scalable to include real datasets like MIMIC-III or eICU

    Easy to modify for multiclass or multi-label problems

🧩 Extensions

    🔄 Add support for multiple chronic conditions

    🎯 Multi-label classification (e.g., diabetes + hypertension)

    🧠 SHAP/Grad-CAM for model explainability

    📊 Integration with Streamlit dashboard

👨‍💻 Author

Developed by [Your Name]
Contact: [you@example.com]
