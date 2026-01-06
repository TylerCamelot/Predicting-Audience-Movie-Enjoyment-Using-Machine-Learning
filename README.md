# What Drives Audience Enjoyment? Predicting Movie Ratings with Machine Learning

## Overview
This project analyzes what factors drive audience enjoyment of movies and evaluates how accurately popular critic platforms predict audience sentiment. While viewers often rely on IMDb or Rotten Tomatoes scores, enjoyment is subjective and influenced by additional movie attributes. This analysis combines critic ratings with structured metadata to improve prediction accuracy and generate actionable insights.

## Problem Motivation
Choosing a movie is a personal and often uncertain decision. Audiences frequently question whether critic ratings truly reflect how much they will enjoy a film. This project addresses:
- Which critic platform (IMDb or Rotten Tomatoes) better predicts audience ratings
- Whether critic ratings alone accurately capture audience enjoyment
- How additional movie attributes can enhance predictive performance

## Data
- Sources: IMDb and Rotten Tomatoes datasets (Kaggle)
- Records: ~3,000 movies
- Target Variable: Audience rating
- Key Features:
  - IMDb and Rotten Tomatoes ratings
  - Budget and runtime
  - Genre and MPAA rating
  - Release timing (seasonality)
  - Critic text sentiment (VADER)
  - Historical director experience

## Feature Engineering
- Log transformation of budget and runtime to address skewness
- Seasonality features based on release timing
- Sentiment analysis of critic reviews using VADER, binned to capture non-linear effects
- Historical director experience metrics to represent reputation effects

## Modeling Approach
Models were evaluated using cross-validation and hyperparameter tuning:
- Linear Regression (baseline)
- Polynomial and Ridge Regression
- Decision Tree Regression
- Random Forest Regression
- KNN Regression
- XGBoost Regression

## Results
- IMDb outperformed Rotten Tomatoes as a predictor of audience ratings (R² = 0.714 vs. 0.544)
- Optimized Random Forest using IMDb alone achieved R² = 0.771
- Fully optimized XGBoost model with engineered features achieved **R² = 0.803**

## Key Insights
- IMDb ratings are a strong indicator of audience enjoyment
- Runtime, budget, critic sentiment, genre, and MPAA rating significantly influence audience ratings
- Combining critic ratings with structured metadata improves prediction accuracy by ~3.2%

## Business Implications
- Audiences can make more informed viewing decisions by considering factors beyond critic scores
- Studios can leverage insights on runtime, budget, sentiment, and release timing to improve audience alignment and engagement

## Limitations
- Risk of overfitting due to extensive hyperparameter tuning
- Dataset size limits generalizability
- Focus on tree-based models may overlook patterns captured by other model families

## Tech Stack
Python · pandas · NumPy · scikit-learn · XGBoost · matplotlib · seaborn · SQL

## My Contributions
- Developed the entire data pipeline and machine learning workflow, including data preprocessing, feature engineering, model training, hyperparameter tuning, and evaluation
- Implemented and optimized all regression models in Python, including Random Forest and XGBoost
- Led and authored Sections 4 and 5 of the final report, covering data analysis, model results, interpretation, and performance comparison

## Contributors
- **Tyler Camelot**
- Ziqi Huang
- Yu-Fang Huang
- Ilnaz Bagheri
- Lasya Reddy Kotha
