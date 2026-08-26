# Laptop Price Prediction

A Machine Learning regression project that predicts **laptop prices based on laptop specifications**.

The project covers data cleaning, EDA, feature engineering, preprocessing, model training, evaluation, and model comparison.

## Project Overview

The goal is to predict laptop prices using features such as:

- Brand
- Processor
- CPU cores
- RAM
- Storage
- Graphics card
- Display size & resolution
- Operating system
- Rating
- Warranty

**Problem Type:** Supervised Machine Learning — Regression
**Target:** `price`

## Dataset

The project uses `laptops_uncleaned.csv`, containing laptop specifications and their corresponding prices.

Important original features include:

`model`, `price`, `rating`, `processor`, `core`, `ram`, `memory`, `graphic_card`, `display`, `os`, `warrenty`

## Workflow

```text
Raw Dataset
    ↓
Data Cleaning
    ↓
EDA
    ↓
Feature Engineering
    ↓
Feature Selection
    ↓
Preprocessing
    ↓
Model Training
    ↓
Evaluation & Comparison
    ↓
Feature Importance
```

## Feature Engineering

The project extracts and creates features such as:

- `brand`
- `processor_brand`
- `core_count`
- `ram`
- `storage_gb`
- `storage_type`
- `has_dedicated_gpu`
- `gpu_vram_gb`
- `screen_size`
- `screen_resolution`
- `os_category`
- `warranty_years`

Price outliers are removed using the **IQR method**, and categorical features are converted using **One-Hot Encoding**.

## Models

Three regression models are compared:

1. **Linear Regression**
2. **Random Forest Regression**
3. **Gradient Boosting Regression**

The data is split into **80% training / 20% testing** using `random_state=42`.

## Evaluation

Models are evaluated using:

- **MAE** — Mean Absolute Error
- **RMSE** — Root Mean Squared Error
- **R² Score**

Lower MAE/RMSE and higher R² indicate better performance.

## EDA

The notebook includes:

- Price distribution
- Rating vs. price
- RAM vs. price
- Brand price analysis
- Correlation heatmap

Feature importance is also analyzed using the **Gradient Boosting** model.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

````

##  Installation & Usage

```bash
git clone https://github.com/marames25/Laptop-Price-Prediction.git
cd Laptop-Price-Prediction

python -m venv venv
````

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run Jupyter:

```bash
jupyter notebook
```

Open `Laptop_Price_Prediction_v2.ipynb` and run the cells sequentially.
