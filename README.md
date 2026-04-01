# Lithology Classification: CNN vs. Random Forest

This project implements and compares two different machine learning approaches—**Convolutional Neural Networks (CNN)** and **Random Forest (RF)**—to classify lithofacies from geological well-log data. The analysis evaluates model performance across both full datasets and filtered datasets to understand the impact of data quality on predictive accuracy.

## Project Overview
Accurate lithology identification is fundamental to reservoir characterization. This repository contains a comparative study using the FORCE 2020 dataset:
- **Spatial Analysis:** Mapping well locations using geospatial coordinates (X, Y).
- **Data Engineering:** Handling missing values in specific logs (SGR, RMIC) and filtering wells based on sample density.
- **Model Comparison:** Testing a depth-sequence-aware CNN against a feature-based Random Forest.

## Model Details
### Random Forest (RF)
- **Type:** Ensemble Learning.
- **Features:** Statistical distributions of logs (GR, RHOB, NPHI, etc.).
- **Purpose:** Serves as a robust baseline for tabular data classification.

### Convolutional Neural Network (CNN)
- **Framework:** PyTorch.
- **Architecture:** 1D Convolutional layers designed to identify vertical patterns and stratigraphic transitions.
- **Input:** 1D windowed segments of well-log data.

## Usage Guide
1. **Data Placement:** Ensure your `CSV_train.csv` or equivalent dataset is in the project directory.
2. **Preprocessing:** Run the initial notebook cells to perform KNN Imputation and feature scaling (Standard or Robust Scaler).
3. **Training:**
   - For RF: Execute the Scikit-Learn training pipeline.
   - For CNN: Convert data to PyTorch tensors and initiate the training loop.
4. **Evaluation:** Review the confusion matrices and F1-score reports provided at the end of each notebook.

## Setup Instructions
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`.
3. Open the `.ipynb` files in Jupyter Lab or VS Code.
