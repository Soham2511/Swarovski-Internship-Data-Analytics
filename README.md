# Swarovski Pearl Yield Prediction

## Overview
This project focuses on predicting manufacturing yield (Okper) in pearl production using machine learning. The goal is to analyze defect patterns, product characteristics, and process data to improve yield prediction and provide actionable insights.

---

## Problem Statement
Manufacturing yield prediction is critical for optimizing production efficiency and reducing waste.  

This project builds a machine learning pipeline to predict the percentage of acceptable pearls (**Okper**) using historical manufacturing data, defect counts, and product attributes.

---

## Dataset
The dataset used in this project is **proprietary** and cannot be shared publicly.

It contains:
- Manufacturing batch information  
- Product and colour codes  
- Defect counts across multiple stages  
- Yield percentage (Okper)  

### Data Access
To run this project, place the dataset files inside the `data/` folder:
```bash
    data/
    │
    ├── cp_results.csv
    ├── colour_code.csv
    ├── product_code.csv
    └── dictionary.csv
```

---

## Project Structure
```bash
swarovski-pearl-yield-prediction/
    ├── README.md
    ├── requirements.txt
    ├── .gitignore

    ├── data/
    ├── notebooks/
    ├── src/
    ├── models/
    ├── results/
    └── reports/
```

---

## Workflow
1. Data Cleaning  
2. Exploratory Data Analysis (EDA)  
3. Outlier Detection  
4. Feature Engineering  
5. Feature Selection  
6. Model Training  
7. Hyperparameter Tuning  
8. Model Evaluation  
9. Feature Importance Analysis  

---

## Models Used
- Linear Regression  
- Ridge / Lasso Regression  
- Random Forest  
- K-Nearest Neighbors  
- XGBoost  
- Stacking Ensemble  

---

## Results
*(Update after final model training)*

- Best Model: XGBoost  
- R² Score: XX  
- MAE: XX  
- RMSE: XX  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  
- SHAP  

---

## Key Highlights
- Domain-driven feature engineering using defect categories  
- Handling of manufacturing process data  
- Ensemble modeling for improved prediction  
- Model interpretability using SHAP  

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-username/swarovski-pearl-yield-prediction.git
cd swarovski-pearl-yield-prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Add dataset to `data/` folder

4. Run notebook:
```bash
notebooks/pearl_yield_analysis.ipynb
```

---

## Future Improvements
- Advanced feature engineering (interaction features, defect ratios)  
- Time-series based modeling  
- Hyperparameter optimization (Optuna)  
- Deployment as a web application  

---

## Author
Soham Jagtap
