# Laptop Price Prediction Using Machine Learning

## Project Overview

This project predicts laptop prices using machine learning based on hardware and specification features such as RAM, storage, processor family, CPU cores/threads, GPU information, display resolution, operating system, and specification rating.

The project demonstrates an end-to-end machine learning workflow:

**Dataset → Data Cleaning → Feature Engineering → EDA → Feature Selection → Preprocessing → Train/Test Split → Model Training → Evaluation → Prediction**

## Objectives

- Clean and prepare laptop specification data.
- Extract useful features from raw specification text.
- Explore relationships between laptop specifications and price.
- Train regression models for price prediction.
- Compare Linear Regression and Random Forest Regression.
- Identify important features used by the Random Forest model.
- Predict the price of a new laptop from its specifications.

## Dataset

The project uses the Kaggle **Laptop Price Prediction Dataset — Exploring Laptop Prices: A Dataset for Predictive Analysis and Price Prediction**.

Place the dataset file named:

```text
laptop_price.csv
```

in the same directory as the Jupyter notebook.

## Main Features

The final model uses 18 features:

- brand
- spec_rating
- Ram
- Ram_type
- ROM
- ROM_type
- display_size
- OS
- warranty
- processor_generation
- processor_brand
- processor_family
- CPU_cores
- CPU_threads
- GPU_brand
- GPU_memory
- GPU_type
- total_pixels

## Models Used

### 1. Linear Regression
Used as a baseline regression model.

### 2. Random Forest Regression
Used as the main nonlinear regression model.

## Results

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | ₹19,075.84 | ₹27,823.30 | 0.7741 |
| Random Forest | ₹12,646.16 | ₹23,017.25 | 0.8454 |

The Random Forest model achieved lower MAE and RMSE and a higher R² score on the same test set.

## Top Feature Importances

The most important transformed features in the Random Forest model included:

1. Total pixels
2. RAM
3. GPU memory
4. Specification rating
5. CPU cores
6. Display size
7. CPU threads
8. ROM

Feature importance describes how the model used the features for prediction; it does not establish causal relationships.

## Example Prediction

For a sample laptop with:

- Brand: HP
- RAM: 16 GB
- Storage: 512 GB
- RAM Type: DDR4
- OS: Windows 11
- Processor: Intel Core i5, 13th generation
- CPU: 10 cores / 12 threads
- GPU: Intel integrated graphics
- Display: 15.6 inches
- Resolution: 1920 × 1080

the model predicted approximately:

**₹75,641.77**

## Installation

Clone or download the repository, then install the dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Open:

```text
Asmita_LaptopPricePrediction.ipynb
```

Make sure `laptop_price.csv` is in the same folder before running the notebook.

## Project Structure

```text
Laptop_Price_Prediction/
│
├── Asmita_LaptopPricePrediction.ipynb
├── requirements.txt
├── Project_Report.docx
├── README.md
└── laptop_price.csv
```

> The dataset file is not included in this submission package unless separately permitted by its source/license. Download the dataset from its original source and place it beside the notebook.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Future Scope

- Hyperparameter tuning
- Cross-validation
- Additional regression algorithms
- A web-based prediction interface
- More recent laptop data
- Model explainability techniques

## Submitted By:

**Asmita**
