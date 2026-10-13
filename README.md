# E-Commerce Dynamic Price Prediction

A machine learning project focused on predicting retail prices for products using a jewelry pricing dataset. The work explores how pricing can be modeled using structured product attributes and compares multiple regression approaches to identify the most accurate and business-relevant forecasting strategy.

This project was developed as part of the IDEAS - Institute of Data Engineering, Analytics and Science Foundation Autumn Internship Program 2026.

## Project Overview

The dataset used in this project is the OpenML `diamonds` dataset, which contains product characteristics such as carat, cut, color, clarity, depth, table, and physical dimensions (`x`, `y`, `z`), along with the target variable `price`.

The objective is to build a data-driven pricing model that can estimate the value of a product based on its measurable attributes. This is useful for understanding how pricing varies with product quality and for creating a retail strategy that minimizes underpricing while avoiding overpricing.

## Business Problem

In e-commerce and retail pricing, a product’s price must balance:

- profit maximization
- customer conversion
- market competitiveness
- demand sensitivity

A predictive model can estimate expected price and help support better pricing decisions. This project treats the problem as a supervised regression task and evaluates model quality using both general metrics and an asymmetric pricing penalty designed to penalize underpricing more heavily.

## Objectives

- Load and inspect the dataset structure
- Perform exploratory data analysis
- Prepare the data for modeling
- Train several regression models
- Evaluate model performance using standard regression metrics
- Measure business-oriented pricing error with an asymmetric loss function
- Segment the market into pricing tiers using unsupervised clustering

## Dataset

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

The dataset contains 53,940 rows and 10 columns, making it suitable for both predictive modeling and pricing analysis.

## Methodology

The notebook follows a structured workflow:

1. Data loading and dimensionality assessment
2. Missing value and data quality checks
3. Feature engineering and preprocessing
4. Train-test split and standardization
5. Baseline model training using Linear Regression
6. Model evaluation using MAE, RMSE, and R²
7. Asymmetric pricing error calculation to reflect profit-sensitive pricing decisions
8. Comparison with additional models such as:
   - Ridge Regression
   - Random Forest Regressor
   - Multi-Layer Perceptron (MLP)
9. Feature importance analysis
10. Market segmentation using K-Means clustering on `carat` and `price`

## Models Used

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- MLP Regressor
- K-Means clustering for market segmentation

## Key Results

The best-performing model in the notebook was the Random Forest Regressor, which achieved:

- R² Score: 0.9814
- Asymmetric Pricing Error: 307.00

The baseline Linear Regression model produced:

- MAE: 599.44
- RMSE: 874.36
- R²: 0.8987

These results show that the non-linear model captures pricing patterns much more effectively than the basic linear baseline.

## Market Segmentation Insight

The notebook also groups products into three pricing tiers based on carat and actual price, then compares average actual versus predicted values in each cluster.

Example segment summary:

- Cluster 0: mean actual price ≈ 1176.83; mean predicted price ≈ 1186.69
- Cluster 1: mean actual price ≈ 4313.42; mean predicted price ≈ 4345.12
- Cluster 2: mean actual price ≈ 8736.53; mean predicted price ≈ 8636.03

This demonstrates that the model remains consistent across low, mid, and premium pricing categories.

## Repository Contents

- `Copy_of_Project_2_E_Commerce_Dynamic_Price_Prediction (1).ipynb` - main analysis notebook
- `README.md` - project documentation

## Setup

Use Python 3.10+ and install the required dependencies.

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## Running the Project

You can open the notebook in any of the following ways:

- Jupyter Notebook / JupyterLab
- VS Code with Python support
- Google Colab by uploading the notebook

```bash
jupyter notebook "Copy_of_Project_2_E_Commerce_Dynamic_Price_Prediction (1).ipynb"
```

## Notes

- The notebook uses `sklearn.datasets.fetch_openml(name='diamonds', as_frame=True)`.
- The project focuses on a practical retail pricing use case rather than a generic regression benchmark.
- The asymmetric error metric is especially useful because it reflects the real business risk of underpricing inventory.

## License

This project is intended for academic and educational use as part of the internship assignment. If you plan to reuse it outside the coursework, confirm the license terms for the underlying dataset and any third-party libraries used.

## Summary

This project demonstrates a complete data science workflow for dynamic pricing prediction in an e-commerce context, from dataset loading and preprocessing to model comparison, evaluation, and segmentation. It shows how machine learning can support better pricing decisions by turning product attributes into actionable price estimates.

## Author
Developed by Rajdeep