# Student Performance Prediction

## Overview
This repository contains a Jupyter Notebook for predicting student performance using a dataset from Kaggle. The notebook performs data loading, exploration, preprocessing, and trains a Linear Regression model to predict the `Performance Index` based on features like study hours and previous scores, achieving an R² score of ~98.84%.

## Dataset
- **Source**: `/kaggle/input/student-performance-dataset/StudentPerformance.csv` (10,000 entries)
- **Features**:
  - `Hours Studied` (numerical, 1-9)
  - `Previous Scores` (numerical, 40-100)
  - `Extracurricular Activities` (Yes/No, encoded as 1/0)
  - `Sleep Hours` (numerical, 4-9)
  - `Sample Question Papers Practiced` (numerical, 0-9)
- **Target**: `Performance Index` (numerical, regression task, 10-100)
- **Preprocessing**: Encode categorical column; no missing values.

## Approach
1. **Data Loading & Exploration**:
   - Load with Pandas; view head, describe, info.
   - Check for nulls (none).
   - Visualize correlation heatmap.

2. **Preprocessing**:
   - Map 'Yes' → 1, 'No' → 0 for Extracurricular Activities.
   - Split into features (X) and target (y).
   - Train-test split (80/20).

3. **Modeling & Evaluation**:
   - Model: LinearRegression (default parameters).
   - Train on training data; predict on test.
   - Metrics: Mean Squared Error (MSE), R-squared (R²).
   - Outputs: Coefficients, Intercept, MSE (~4.23), R² (~98.84%).

## Requirements
- Python 3.10+
- Libraries: `numpy`, `pandas`, `seaborn`, `matplotlib`, `scikit-learn`

Install via:
```bash
pip install numpy pandas seaborn matplotlib scikit-learn
```

## Results
- MSE: ~4.23
- R² Score: ~98.84%
- Coefficients: [2.85, 1.02, 0.65, 0.48, 0.19]
- Intercept: ~-34.05

## Notes
- Optimized for Kaggle environment; adjust paths for local use.
- High R² indicates strong linear relationships; potential for more models or tuning.

