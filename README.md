# 💎 E-Commerce Dynamic Price Prediction

A data science and machine learning project designed to predict retail product prices using product attributes from the `diamonds` dataset. The goal is to build a pricing model that supports smarter online retail decisions, improves value estimation, and reduces pricing risks such as underpricing.

This project was developed as part of the IDEAS - Institute of Data Engineering, Analytics and Science Foundation Autumn Internship Program 2026.

## 🌟 Project Snapshot

- 🧠 Problem Type: Supervised regression
- 📦 Dataset: OpenML `diamonds`
- 🎯 Target Variable: `price`
- 🏬 Use Case: Dynamic pricing for e-commerce / retail products
- 📈 Best Model: Random Forest Regressor

## 🧩 Business Problem

In real-world e-commerce pricing, a product must be priced to balance:

- 💰 Profitability
- 🛍️ Customer conversion
- 📉 Market competitiveness
- 📊 Demand sensitivity

A predictive model helps estimate the likely fair price based on product characteristics, reducing guesswork and improving pricing strategy.

## 🎯 Objectives

- 🔍 Load and inspect the dataset
- 🧹 Clean and prepare the data
- 📊 Explore feature relationships
- 🧠 Train multiple regression models
- ✅ Evaluate performance using standard metrics
- ⚠️ Measure asymmetric business loss for pricing risk
- 🧭 Segment products into pricing tiers using clustering

## 🗂️ Dataset Overview

Source: OpenML `diamonds` dataset

Key features:

- `carat`
- `cut`
- `color`
- `clarity`
- `depth`
- `table`
- `x`, `y`, `z`

Target variable:

- `price`

Dataset stats:

- 📏 Rows: 53,940
- 📐 Columns: 10

## 📊 Workflow Infographic

```mermaid
flowchart LR
    A[📥 Load Dataset] --> B[🧹 Data Cleaning]
    B --> C[📊 EDA & Feature Analysis]
    C --> D[🛠️ Preprocessing + Split]
    D --> E[🤖 Train Models]
    E --> F[📈 Evaluate Metrics]
    F --> G[💸 Asymmetric Pricing Error]
    G --> H[🧭 Market Segmentation]
    H --> I[✅ Insights & Recommendations]
```

## 🧪 Models Used

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- Multi-Layer Perceptron (MLP)
- K-Means clustering

## 📈 Key Results

### Baseline Linear Regression

- MAE: 599.44
- RMSE: 874.36
- R²: 0.8987

### Best Model: Random Forest Regressor

- R² Score: 0.9814
- Asymmetric Pricing Error: 307.00

### Why this matters

- 📉 Lower RMSE means better price prediction accuracy
- 💡 Higher R² means the model explains more variation in pricing
- 🏷️ The asymmetric error penalizes underpricing more strongly, which is valuable in real business settings

## 🧭 Market Segmentation Insight

The notebook also segments products into three pricing tiers using K-Means clustering based on `carat` and `price`.

Example summary:

- 🟢 Cluster 0: Actual ≈ 1176.83 | Predicted ≈ 1186.69
- 🟡 Cluster 1: Actual ≈ 4313.42 | Predicted ≈ 4345.12
- 🔴 Cluster 2: Actual ≈ 8736.53 | Predicted ≈ 8636.03

This shows that the pricing model remains consistent across low, mid, and premium price segments.

## 📁 Repository Contents

- `Copy_of_Project_2_E_Commerce_Dynamic_Price_Prediction (1).ipynb` — main notebook with all analysis and modeling steps
- `README.md` — project documentation

## ⚙️ Setup

Use Python 3.10+ and install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## ▶️ How to Run

Open the notebook in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

```bash
jupyter notebook "Copy_of_Project_2_E_Commerce_Dynamic_Price_Prediction (1).ipynb"
```

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📝 Notes

- The notebook uses `fetch_openml(name='diamonds', as_frame=True)`.
- The model focuses on practical retail pricing rather than generic regression benchmarking.
- The custom asymmetric error metric is useful because underpricing has a stronger business impact than overpricing.

## 📜 License

This project is intended for academic and educational use as part of the internship assignment. If reused outside the coursework, please review the licensing terms for the dataset and third-party libraries involved.

## ✅ Final Summary

This project demonstrates a complete machine learning workflow for e-commerce pricing prediction, covering:

- 📥 data acquisition
- 🧮 preprocessing
- 🤖 model training
- 📊 evaluation
- 💸 business-aware metrics
- 🧭 customer/market segmentation

It highlights how predictive analytics can help businesses make smarter pricing decisions and improve revenue strategy.

## Author
Developed by Rajdeep
