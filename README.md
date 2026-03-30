# Global Terrorism Database (GTD) Analysis & Predictive Modeling

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-FF9F00?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-000000?style=for-the-badge&logo=statsmodels&logoColor=white)

**End-to-End Data Science Project** analyzing over **181,691 terrorist incidents** (1970–2017) using advanced preprocessing, visualization, machine learning, and forecasting techniques.

## 📊 Project Overview

This project performs comprehensive analysis on the **Global Terrorism Database (GTD)** — one of the most detailed open-source terrorism datasets in the world. The focus was to clean messy real-world data, uncover hidden patterns, and build robust predictive models to support data-driven counter-terrorism insights.

The pipeline includes heavy data preprocessing, interactive search tools, exploratory data analysis, classification, association rule mining, and time series forecasting.

---

## 🎯 Objectives

- Perform extensive data cleaning and preprocessing on a large, noisy dataset
- Identify temporal, geographical, and tactical patterns in global terrorism
- Build machine learning models to predict attack success and high-risk regions
- Discover meaningful associations between attack types and targets
- Forecast future terrorism-related deaths using time series modeling

---

## 📁 Dataset

- **Source**: Global Terrorism Database (GTD) by START Consortium
- **Size**: 181,691 rows × 135 columns
- **Time Period**: 1970 – 2017
- **Key Features**: Date, Country, Region, Attack Type, Target Type, Terrorist Group, Killed, Wounded, Latitude, Longitude, etc.

---

## 🔧 Methodology

1. **Data Preprocessing**
   - Dropped 34 irrelevant/redundant columns
   - Handled missing values strategically (`'Unknown'` for categorical, `0` for casualties)
   - Created new feature: `Casualties = Killed + Wounded`
   - Renamed columns for readability
   - Removed duplicate records
   - Built an **Interactive Search System** for easy dataset querying

2. **Exploratory Data Analysis (EDA)**
   - Time-series trends of casualties
   - Top countries, regions, attack types, and groups
   - Geospatial visualization using Folium

3. **Modeling & Analysis**
   - Classification with Random Forest
   - Association Rule Mining (Apriori)
   - Time Series Forecasting (SARIMA)

---

## 🚀 Key Features & Achievements

- Reduced dataset complexity while preserving analytical power
- Developed an **interactive search tool** allowing users to query by Event ID, Country, or Group
- Created insightful visualizations (line plots, bar charts, interactive maps)
- Handled severe class imbalance using **SMOTE** and `class_weight='balanced'`
- Ensured no target leakage and performed proper model validation

---

## 🤖 Models Built

### 1. Attack Success Prediction
- **Model**: Random Forest Classifier + **SMOTE**
- **Why?** Robust with high-dimensional categorical data + built-in feature importance
- **Performance**: **98.39% Accuracy**, 99% Recall (Successful Attacks)
- **Key Features**: Casualties, Attack Type, Target Type, Region, Group

### 2. High-Risk Region Classification
- **Model**: Random Forest Classifier (`class_weight='balanced'`)
- **Why?** Excellent for highly imbalanced data and interpretability
- **Performance**: **99.99% Accuracy**, 0.9998 OOB Score
- **Target**: Regions with >500 attacks labeled as high-risk

### 3. Association Rule Mining
- **Model**: Apriori Algorithm (mlxtend)
- **Why?** Discovers interpretable "if-then" relationships for policy use
- **Key Finding**: Strong rule "Government → Assassination" (Lift = 4.105)

### 4. Time Series Forecasting
- **Model**: **SARIMA**
- **Forecast Period**: 2018–2020 (36 months)
- **Prediction**: **28,458 total deaths**
- **Evaluation**: MAE = 62.55 | RMSE = 142.63

---

## 📈 Results & Insights

- **Iraq** recorded the highest number of casualties
- Most common attack type: **Bombing/Explosion**
- Sharp increase in terrorism after 2010, peaking in **2014**
- **Taliban** identified as the most active group
- Strong associations found between attack types and specific targets
- Successful forecasting of monthly terrorism-related deaths

---

## 🛠️ Technologies Used

- **Programming**: Python 3
- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn, Folium
- **Machine Learning**: Scikit-learn, SMOTE, mlxtend
- **Time Series**: Statsmodels (SARIMA)
- **Others**: Interactive Python functions

---

## 📊 Insights & Visualizations

- Line plot showing casualty trends over time
- Top 15 countries by total casualties
- Most frequent attack types
- Interactive geospatial map of terrorist incidents
- Feature importance plots from Random Forest models
- Association rules with support, confidence, and lift
