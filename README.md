# 🌧️ Flood Prediction System – Bandar Lampung

**Predicting flood events using meteorological data and machine learning.**  
An **end-to-end Data Science project** that applies the **Random Forest Classifier** to predict flood occurrences in **Bandar Lampung (2010–2020)** based on key weather indicators.

![Correlation Matrix](img/correlation_matrix.png)
![Feature Importance](img/feature_importance.png)

---

## Project Overview

This project focuses on developing a **Flood Prediction Model for Bandar Lampung** using data science and machine learning techniques.  
The goal is to identify key meteorological factors influencing flood events and to build a model that supports **early warning systems** for disaster prevention and decision-making.

The project follows an **end-to-end data science workflow**, covering:
1. Data understanding  
2. Preprocessing & feature engineering  
3. Model development (Random Forest Classifier)  
4. Model evaluation (Accuracy, Recall, Precision, AUC-ROC)  
5. Visualization and interactive dashboard deployment

---

## Key Insights

| Factor | Correlation with Flood |
|--------|------------------------|
| **Weekly Rainfall** | **1.00 (Strongest Predictor)** |
| **Daily Rainfall** | 0.76 |
| **Humidity** | 0.74 |
| **Air Temperature** | 0.63 |

> High rainfall accumulation, elevated humidity, and increased temperature strongly correlate with flood occurrence in Bandar Lampung.

---

## Data Description

The dataset contains **historical meteorological observations and flood event records** collected from **Bandar Lampung** between **2010 and 2020**.  
It includes daily and weekly weather variables such as:
- Air Temperature (°C)  
- Humidity (%)  
- Rainfall (mm)  
- Surface and Monsoon Wind Direction  
- Temporal features (Year, Month, Day)

> The data was cleaned, standardized, and normalized for modeling purposes to ensure analytical consistency and predictive accuracy.

---

## Data Preparation

- Checked and removed missing or duplicate entries  
- Standardized numerical formats (decimal normalization)  
- Normalized values into 0–1 range  
- Extracted temporal features from the date column (`Year`, `Month`, `Day`)  
- Performed correlation analysis to select the most influential features  

---

## Model Specification

| Component | Description |
|------------|-------------|
| **Algorithm** | Random Forest Classifier |
| **Estimators** | 50 trees |
| **Weights** | Balanced class weights |
| **Validation** | Stratified 5-Fold Cross Validation |
| **Split Ratio** | 70% Train / 30% Test |
| **Libraries** | pandas, numpy, scikit-learn, matplotlib, seaborn |

---

## Evaluation Results

| Metric | Score |
|--------|--------|
| **Accuracy** | 93.3% |
| **Recall** | 100% |
| **Precision** | 85.7% |
| **AUC-ROC** | 94.4% |
| **OOB Score** | 97% |
| **Mean Cross-Validation Score** | 90% |

> ✅ The model successfully identified **all flood cases (Recall 1.0)** while maintaining **high precision** and **excellent generalization** performance.

---

## Feature Importance

| Rank | Feature | Importance Score |
|------|----------|------------------|
| 1 | Total Rainfall (mm) | 0.55 |
| 2 | Humidity (%) | 0.15 |
| 3 | Air Temperature (°C) | 0.13 |
| 4 | Year | 0.05 |
| 5 | Weekly Rainfall | 0.04 |
| 6 | Surface Wind | 0.03 |
| 7 | Month | 0.02 |
| 8 | Monsoon Wind Direction | 0.02 |
| 9 | Day | 0.01 |

> 💡 **Rainfall** remains the most dominant factor influencing flood prediction in Bandar Lampung.

---

## Interactive Dashboard

A responsive dashboard was built using **Tailwind CSS** and **Chart.js**, providing real-time visualization of:
- Model performance metrics (accuracy, recall, precision, AUC)
- Feature importance analysis
- Confusion matrix
- Correlation matrix
- Cross-validation and OOB score results

### Demo File:
> [index.html](./index.html)

**Preview:**
![Dashboard Preview](./preview-dashboard.png)

---

## Project Architecture
