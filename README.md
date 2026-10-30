#  Pineapple Disease Risk Prediction Using Machine Learning

A machine learning classification project that analyzes environmental and soil conditions to predict possible disease risk in pineapple farms. This project demonstrates how data science can support agricultural monitoring and decision-making in the Philippines.

---

##  Project Overview

The Philippines is an agricultural country where pineapple is one of the important crops produced in different regions. However, pineapple production may be affected by crop diseases and environmental conditions that influence plant health and growth.

This project uses machine learning classification algorithms to analyze five environmental and soil factors: temperature, humidity, soil moisture, rainfall, and soil pH. Based on these features, the models classify pineapple farm conditions into two categories: **Low Disease Risk** and **High Disease Risk**.

The main goal is to demonstrate how machine learning can help identify conditions associated with possible crop disease risk and support better farm monitoring and management decisions.

##  Objectives

- Use a synthetic dataset representing different pineapple farm conditions.
- Explore and analyze environmental and soil factors using Exploratory Data Analysis (EDA).
- Preprocess the dataset and prepare it for machine learning.
- Train and compare different classification algorithms.
- Evaluate model performance using classification metrics.
- Identify the best-performing model for predicting pineapple disease risk.
- Allow users to test the trained model using their own input values.

##  Dataset Description

The dataset contains **2,000 synthetically generated records** with six columns, consisting of five input features and one target variable.

| Feature | Description | Unit |
|---|---|---|
| `temperature_c` | Temperature of the farm environment | °C |
| `humidity_pct` | Relative humidity level | % |
| `soil_moisture_pct` | Amount of moisture in the soil | % |
| `rainfall_mm` | Amount of rainfall | mm |
| `soil_ph` | Acidity or alkalinity level of the soil | pH |
| `disease_risk` | Target variable representing disease risk | 0 or 1 |

### Target Variable

| Value | Category |
|---|---|
| 0 | Low Disease Risk |
| 1 | High Disease Risk |

**Note:** The dataset is synthetically generated using Python and NumPy. It does not contain actual records from Philippine pineapple farms. The target labels represent simulated disease risk and are not validated agricultural diagnoses.

##  Exploratory Data Analysis (EDA)

The dataset undergoes Exploratory Data Analysis to better understand its characteristics and identify patterns.

The analysis includes:

- Checking dataset size and data types.
- Identifying missing values and duplicate records.
- Generating summary statistics.
- Examining feature distributions using histograms.
- Visualizing relationships between features using a correlation heatmap.
- Checking the distribution of Low Risk and High Risk categories.

##  Data Preprocessing

Before training the models, the dataset undergoes the following preparation steps:

- Removing duplicate records.
- Handling missing numerical values using median imputation.
- Separating input features and the target variable.
- Splitting the dataset into 80% training data and 20% testing data.
- Applying feature scaling where needed.

##  Machine Learning Algorithms

Five classification algorithms are used and compared in this project.

| Algorithm | Hyperparameters |
|---|---|
| Logistic Regression | `C` |
| Random Forest | `n_estimators`, `max_depth` |
| Support Vector Machine (SVM) | `C`, `kernel` |
| K-Nearest Neighbors (KNN) | `n_neighbors`, `weights` |
| Decision Tree | `max_depth`, `min_samples_split` |

Hyperparameter tuning is performed to find suitable settings for each model and improve classification performance.

##  Model Evaluation

The trained models are evaluated and compared using the following metrics:

| Evaluation Metric | Purpose |
|---|---|
| Accuracy | Measures the overall percentage of correct predictions. |
| Precision | Measures how many predicted High Risk cases are actually classified as High Risk. |
| Recall | Measures how many actual High Risk cases are correctly identified. |
| F1-Score | Balances precision and recall. |
| Confusion Matrix | Shows correct and incorrect predictions for each class. |

### Best-Performing Model

Based on the model evaluation results, **Support Vector Machine (SVM)** achieved the best performance among the classification algorithms tested.

SVM was selected as the final model for predicting Low Disease Risk and High Disease Risk categories.

##  Technologies and Libraries

- **Python** – Main programming language.
- **Google Colab** – Development and execution environment.
- **Pandas** – Dataset creation and manipulation.
- **NumPy** – Numerical operations and synthetic data generation.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical charts and correlation heatmaps.
- **Scikit-learn** – Data preprocessing, classification, hyperparameter tuning, and model evaluation.

##  Project Files

| File | Description |
|---|---|
| `generate_dataset.py` | Python code used to generate the synthetic dataset. |
| `pineapple_disease_risk.csv` | Generated dataset containing 2,000 records. |
| `pineapple_disease_classification.ipynb` | Google Colab notebook containing EDA, preprocessing, model training, evaluation, and interactive predictions. |
| `README.md` | Documentation and overview of the project. |

##  How to Run the Project

1. Clone or download this repository.
2. Open `pineapple_disease_classification.ipynb` using [Google Colab](https://colab.research.google.com/).
3. Make sure the dataset is accessible through the provided GitHub raw CSV link.
4. Run the notebook cells in order.
5. Review the EDA results and model performance comparisons.
6. Use the interactive prediction section to enter farm condition values and obtain a predicted disease risk category.

##  Project Significance

This project demonstrates the potential of machine learning in Philippine agriculture. By analyzing environmental and soil conditions, it provides an educational example of how data-driven approaches can support crop monitoring, risk awareness, and farm management.

The project also provides an opportunity to understand how different classification algorithms work and how their performance can be compared to select a suitable model.

##  Limitations

- The dataset is artificially generated and does not represent actual pineapple farm records.
- The disease risk labels are based on simulated conditions and not confirmed crop disease observations.
- The model has not been validated using real-world agricultural data.
- Predictions should not be used as a substitute for professional agricultural assessment or actual disease diagnosis.

---

*This project was developed for educational and academic purposes to demonstrate the application of data science and machine learning in agriculture.*
