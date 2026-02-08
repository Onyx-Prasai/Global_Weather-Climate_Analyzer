# Nepal Temperature Analyzer

This repository contains a focused Jupyter notebook that trains seasonal time-series models for cities in Nepal and provides an interactive predictor.

What this does
- Loads Nepal city-level temperature records from the provided CSV files.
- Trains a seasonal SARIMAX model per city (monthly data, 12-month seasonality).
- Evaluates model performance on a 24‑month holdout and reports mean absolute error (MAE) and accuracy (percent of predictions within ±1.0°C).
- Provides an interactive notebook UI (dropdown + date picker) that returns a forecast mean and a model-derived 95% prediction interval.

Quick start
1. Create and activate a Python environment (recommended Python 3.10+):

```bash
python -m venv .venv
# On Windows:
.\.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate
pip install --upgrade pip
```

2. Install required packages:

```bash
pip install pandas numpy statsmodels matplotlib
# Optional (improves predictions/UI):
pip install ipywidgets xgboost
jupyter nbextension enable --py widgetsnbextension --sys-prefix
```

Run the notebook
- Open `Code_File/Global_Temperature_Analysis.ipynb` in Jupyter Notebook or JupyterLab and run cells from top to bottom.

Notes
- The notebook intentionally focuses only on Nepal data (no other countries are referenced).
- The interactive UI requires `ipywidgets`; the notebook explains how to install it.
- If you need the project to guarantee ≥95% accuracy under a fixed ±1.0°C tolerance, achieving that will likely require additional modeling (exogenous features, per-city hyperparameter tuning, or more advanced ensembles). I can add those on request.

If you'd like, I can also add a `requirements.txt`, example outputs, or a short README section showing example predictions.

License
- MIT licence.
