# Gold & Nasdaq Time-Series Prediction (LMMSE + GRU)

This repository contains a Jupyter notebook that explores **two different approaches to time-series prediction** on financial data:

- **LMMSE (Linear Minimum Mean Square Error)** prediction using an autocorrelation-based linear filter
- **Deep Learning (GRU)** model trained on sliding windows of the time series

The notebook runs the full pipeline end-to-end: **data loading (Kaggle)** → **preprocessing** → **model training** → **prediction plots / R² & MSE** → and a **simple trading simulation** (threshold-based buy/sell with an optional stop-loss).

> ⚠️ This is an educational project, not financial advice.

## What’s inside

- Gold price data loading and train/test split (rolling multi-year window)
- Nasdaq data loading and cleaning (interpolation for missing values)
- LMMSE filter design + evaluation
- GRU model definition + training
- Prediction comparison (LMMSE vs GRU)
- A small trading simulation loop driven by predicted vs actual price

## Requirements

- Python 3.9+ recommended
- `numpy`, `pandas`, `matplotlib`
- `tensorflow` (Keras)
- `kagglehub` (to fetch datasets)

Example install:

```bash
pip install numpy pandas matplotlib tensorflow kagglehub
```

## Kaggle credentials

The notebook uses `kagglehub` to download datasets. **Do not hardcode your Kaggle API key in the notebook.**
Set these environment variables instead:

```bash
export KAGGLE_USERNAME="<your_username>"
export KAGGLE_KEY="<your_key>"
```

## Running

Open and run the notebook:

```bash
jupyter notebook Gold_Nasdaq_Prediction.ipynb
```
