# Beat the Bookie — EPL Match Outcome Prediction

A machine learning research project for predicting English Premier League (EPL) match outcomes using historical football statistics, engineered team-performance metrics, weather data, Elo ratings, and external contextual features.

This project explores the application of supervised machine learning and feature engineering to sports analytics, comparing multiple classical ML and deep learning models for multi-class football match prediction.

---

## Overview

The goal of this project is to predict EPL match results:

- `H` — Home Win
- `A` — Away Win
- `D` — Draw

Using historical Premier League data spanning over 24 seasons, we expanded the original dataset from **22** to **66 engineered features** by integrating multiple external data sources and advanced statistical metrics. 

The project evaluates multiple classical machine learning and deep learning approaches for football match prediction and comparative model analysis.

---

## Key Features

- Multi-class football outcome prediction
- Feature engineering across historical and contextual data
- Elo rating implementation
- Weather and morale analysis
- Referee bias metrics
- Team seasonal-performance modelling
- Cross-validation and hyperparameter tuning
- Comparative evaluation across 7 ML models

---

## Dataset Engineering

The original dataset contained:
- **8,840 matches**
- **22 features**

We expanded the dataset to:
- **66 engineered features**

### Data Sources

- Open-Meteo weather API
- Football Manager 2024 player database
- FBRef
- FootyStats


---

## Engineered Features

### Team Performance Metrics
- Offensive efficiency
- Defensive efficiency
- Shot conversion rates
- Possession indicators

### Elo Rating System
Implemented a custom Elo rating system to model relative team strength dynamically across seasons.

### Morale System
Designed a morale-scoring mechanism using outcomes from the previous five matches to model psychological momentum. 

### Referee Bias Metrics
Created custom referee-bias indicators using:
- fouls,
- yellow cards,
- red cards,
- penalty tendency differences.


### Environmental Features
Integrated:
- temperature,
- rainfall,
- snowfall,
- wind-speed data

to investigate weather effects on match outcomes.

---
## Feature Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/83631a25-154b-4f1e-8f7a-e2087a9037f5" width="70%" />
  <br>
  <em>Feature-importance analysis across engineered match-performance metrics.</em>
</p>

---

## Machine Learning Models

The following models were trained and evaluated:

1. Logistic Regression
2. Gaussian Naive Bayes
3. Random Forest
4. Support Vector Machine (SVM)
5. XGBoost
6. Multilayer Perceptron (MLP)
7. Long Short-Term Memory (LSTM)

---

## Training & Validation

### Techniques Used

- RandomizedSearchCV
- 5-fold cross-validation
- Hyperparameter tuning
- Early stopping
- Feature selection
- StandardScaler normalization
- One-hot encoding



---

## Important Note on Outcomes

The project later identified potential risks of data leakage caused by highly correlated match-specific efficiency features, which may have artificially inflated evaluation accuracy. 

The project therefore serves primarily as:
- an exploration of feature engineering,
- ML experimentation,
- model evaluation methodologies,
- sports analytics pipelines,

rather than a production-ready betting system.


---

## Technologies

### Languages
- Python

### Libraries
- scikit-learn
- XGBoost
- PyTorch
- pandas
- NumPy
- matplotlib

### ML Techniques
- Classification
- Feature Engineering
- Hyperparameter Optimization
- Cross Validation
- Time-Series Processing

---

## Repository Structure

```text
├── data/
├── preprocessing/
├── feature_engineering/
├── training/
├── evaluation/
├── visualizations/
├── notebooks/
└── README.md
```

---

## Future Improvements

Potential future work includes:
- injury and transfer-window modelling,
- betting odds integration,
- temporal graph modelling,
- transformer-based sequence models,
- improved leakage prevention,
- live prediction pipelines.

---

## Key Learnings

This project highlighted practical machine learning challenges including:
- feature leakage,
- overfitting risks,
- temporal data handling,
- feature-selection trade-offs,
- evaluation reliability in sports prediction systems.

The project reinforced the importance of careful validation and robust feature engineering when building predictive ML pipelines.

---

## Team Project

Developed collaboratively as part of a UCL Computer Science machine learning project.

My contributions focused on:
- feature engineering,
- data preprocessing,
- model experimentation,
- evaluation and validation workflows.

--- 

## Repository Note

This repository primarily showcases the project methodology, feature-engineering process, and evaluation workflow. Portions of the original coursework implementation and datasets are excluded or simplified.
