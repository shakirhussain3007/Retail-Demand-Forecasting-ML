# Retail Demand Forecasting & Stockout Risk Prediction

## Project Overview

This project uses Machine Learning to solve two retail problems:

1. **Demand Forecasting:** Predicting next-day product sales.
2. **Stockout Risk Prediction:** Predicting whether a product may go out of stock the next day.

## Dataset

- Dataset: FreshRetailNet-50K
- Source: [Hugging Face](https://huggingface.co/datasets/Dingdong-Inc/FreshRetailNet-50K)
- Original Records: 4.5 Million
- Stores: 898
- Products: 865
- Time Period: 90 Days

## 1. Demand Forecasting

**Objective:** Predict next-day sales using historical sales data.

### Features
- Lag 1
- Lag 7
- Lag 14
- Rolling Mean 7

### Models Tested

| Model | MAE | R² |
|---|---:|---:|
| Naive Baseline | 0.5105 | 0.7591 |
| Linear Regression V1 | 0.3880 | 0.8631 |
| HistGradientBoosting | 0.4066 | 0.7884 |
| Linear Regression V2 | 0.3910 | 0.8625 |
| Ridge Regression | 0.3922 | 0.8599 |

**Selected Model:** Linear Regression V1

- MAE: 0.3880
- RMSE: 0.6392
- R²: 0.8631
- WAPE: 34.64%

## 2. Stockout Risk Prediction

**Objective:** Predict next-day stockout risk.

### Target Labels
- 0 = No Stockout
- 1 = Stockout

**Model:** Logistic Regression

### Results

| Metric | Score |
|---|---:|
| Accuracy | 64.72% |
| Precision | 60.12% |
| Recall | 54.10% |
| F1 Score | 56.95% |
| ROC-AUC | 66.45% |

## Exploratory Data Analysis

- Total Sales: 4,493,660.787
- Average Daily Sales: 49,929.56
- Highest Sales Day: May 12, 2024
- Lowest Sales Day: March 29, 2024
- Identified the top 10 best-selling products.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Joblib
- Hugging Face Datasets
- Google Colab

## Project Structure

```text
Retail-Demand-Forecasting/
├── Retail_ML_Project.ipynb
├── README.md
```

## How to Run

1. Clone this repository.
2. Install the required libraries.
3. Open the notebook in Google Colab or Jupyter Notebook.
4. Load the dataset from Hugging Face.
5. Run the notebook cells in order.

## Limitations and Future Work

- Improve stockout prediction performance.
- Test additional machine learning algorithms.
- Validate models using local retail business data.
- Integrate models into an inventory management system.

**Note:** These are initial dataset-based experiments and require further validation before real-world deployment.

## Author

Shakir Hussain