# 🌧️ Flood Prediction System – Bandar Lampung

**Predicting flood events using meteorological data and machine learning.**  
An **end-to-end Data Science project** utilizing **Python** and **Random Forest Classifier** to predict flood occurrences in **Bandar Lampung (2010–2020)** based on key weather indicators.

<p align="center">
  <img src="img/correlation_matrix.png" alt="Correlation Matrix" width="450"/>
  <img src="img/feature_importance.png" alt="Feature Importance" width="450"/>
</p>

<p align="center"><em>Figure: Correlation heatmap and feature importance visualization from the flood prediction model.</em></p>

---

## Project Overview

This project aims to develop a **flood prediction model** for Bandar Lampung using **data science and machine learning techniques**.  
The main objectives are:
- To identify the most significant meteorological variables affecting flood occurrence.  
- To build a predictive model that supports **early warning and disaster management systems**.

The workflow follows an **end-to-end data science pipeline**, including:
1. Data understanding and exploration  
2. Data preprocessing and feature engineering  
3. Model development using Random Forest  
4. Model evaluation and validation  
5. Result visualization and dashboard deployment  

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

The dataset contains **historical meteorological observations and flood event records** from **Bandar Lampung (2010–2020)**, including:

- Air Temperature (°C)  
- Humidity (%)  
- Rainfall (mm/day and mm/week)  
- Surface Wind Direction & Monsoon Pattern  
- Temporal Features (Year, Month, Day)

> Data was cleaned, standardized, and normalized to ensure analytical consistency and model reliability.

---

## Data Preparation & Tools

Data preprocessing and transformation were performed using **Python** with the following libraries:

| Step | Tools / Libraries | Description |
|------|--------------------|--------------|
| Data Cleaning | `pandas`, `numpy` | Handling missing values, duplicates, and formatting inconsistencies |
| Feature Engineering | `datetime`, `pandas` | Extracting `year`, `month`, `day` features from date columns |
| Data Normalization | `sklearn.preprocessing` | Scaling features to 0–1 range for consistent model training |
| Exploratory Analysis | `matplotlib`, `seaborn` | Visualizing distributions, correlations, and relationships |
| Feature Selection | `sklearn.feature_selection`, `pandas.corr()` | Identifying top predictors of flood events |

> The correlation matrix (above) shows rainfall, humidity, and temperature as the most influential features.

---

## Model Specification

| Component | Description |
|------------|-------------|
| **Algorithm** | Random Forest Classifier |
| **Estimators** | 50 trees |
| **Weights** | Balanced class weights |
| **Validation** | Stratified 5-Fold Cross Validation |
| **Split Ratio** | 70% Train / 30% Test |
| **Libraries** | `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn` |

---

## Evaluation Results

| Metric | Score |
|--------|--------|
| **Accuracy** | 93.3% |
| **Recall** | 100% |
| **Precision** | 85.7% |
| **AUC-ROC** | 94.4% |
| **OOB Score** | 97% |
| **Cross-Validation Mean** | 90% |

> The model successfully identified **all flood cases (Recall = 1.0)** while maintaining high precision and excellent generalization performance.

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
| 8 | Monsoon Direction | 0.02 |
| 9 | Day | 0.01 |

> 💡 **Rainfall** is the most dominant factor influencing flood risk in Bandar Lampung.

---

## Interactive Dashboard

A responsive web-based dashboard was developed using **Tailwind CSS** and **Chart.js** to visualize key model results and insights.

**Features displayed:**
- Model performance metrics (Accuracy, Recall, Precision, AUC)
- Feature importance ranking  
- Confusion matrix visualization  
- Correlation matrix  
- Cross-validation and OOB performance  

### 🔗 Demo:
> [index.html](./index.html)

<p align="center">
  <img src="./preview-dashboard.png" alt="Flood Prediction Dashboard Preview" width="700"/>
</p>

<p align="center"><em>Figure: Interactive dashboard visualizing key model performance and feature influence metrics.</em></p>

---

## Project Architecture
