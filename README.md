# Installation & Run (Short Guide)

## 1) Install required packages

```bash
pip install numpy pandas yfinance joblib scikit-learn tensorflow seaborn matplotlib
```

## 2) Dataset

**NASDAQ (^IXIC) historical data** is downloaded automatically via `yfinance.download()` in both notebooks. No manual download needed.

## 3) Set output paths in training notebook

Open `Training.ipynb` and update:

- `ModelPath = "YOUR_PATH"`
- `jobLibPath = "YOUR_PATH"`

Example values:

- `ModelPath = "model_nasdaq_hybrid.keras"`
- `jobLibPath = "scaler_nasdaq_hybrid.joblib"`

## 4) Train the model

Run all cells in `Training.ipynb` from top to bottom.

## 5) Test the model

In `Testing.ipynb`, ensure these filenames match your saved outputs:

- `load_model("model_nasdaq_hybrid.keras")`
- `joblib.load("scaler_nasdaq_hybrid.joblib")`

Run all cells in `Testing.ipynb` to get MAPE and the prediction plot.
