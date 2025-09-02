# SA Stocks Volatility & Return Regression

**Volatility Regression**
**Exploratory Data Analysis**

## 📁 Repository Structure (recommended)

```
.
├── data/
│   └── SAStockMarket1998-2024.csv        # Place your CSV(s) here (not included)
├── notebooks/
│   └── SA_Stocks_Volatility_Regression.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## 📊 Project Overview

- **Goal:** Model short‑horizon returns (e.g., 30‑day, 60‑day) and price volatility for selected JSE tickers.
- **Approach:** Time‑series cross‑validation with scikit‑learn pipelines; standardization; regression models.
- **Inputs:** Historical OHLCV or adjusted close series aggregated into engineered features.
- **Outputs:** Metrics such as R² / RMSE / MAE and diagnostic plots.

> Tip: In your notebook, set `CSV_PATH = "data/SAStockMarket1998-2024.csv"` so it works inside this repo.

## 🔧 Setup

1) **Create and activate a virtual environment**  
   **macOS / Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

   **Windows (PowerShell)**
   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

2) **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3) **Prepare data**
   - Create a `data/` folder at the repository root.
   - Copy your CSV(s) into `data/` (e.g., `data/SAStockMarket1998-2024.csv`).

4) **Run the notebook**
   ```bash
   jupyter lab   # or: jupyter notebook
   ```
   Open `notebooks/SA_Stocks_Volatility_Regression.ipynb` and run all cells.

## 🧪 Reproducibility Notes

- Set a fixed `RSEED` (e.g., 42) for any randomized splits or model components.
- Use `TimeSeriesSplit` (or equivalent) to avoid look‑ahead bias.
- Keep your data path **relative** (e.g., `data/...`) rather than a cloud‑specific path.

## 📈 Results (fill in after running)

- Summary of best models and metrics (R², RMSE, MAE).  
- Key figures: feature importance (if applicable), prediction vs. actual plots, residuals.  
- Observations about overfitting, stationarity, and leakage checks.

## 🗂 Data

- **Source:** Replace this with the data source and license.
- **Schema:** Document the columns used (date, ticker, open/high/low/close/volume, etc.).
- **Preprocessing:** Note any cleaning steps (missing values, splits, resampling).

> **Large files:** If any CSV exceeds **100 MB**, use **Git LFS** (see below).

## 📦 Git LFS (optional but recommended for large CSVs)

```bash
git lfs install
git lfs track "*.csv"
git add .gitattributes
```

## 📝 How to Cite / Acknowledge (optional)

If you use this code in academic work, please cite appropriately. 
### BibTeX
```bibtex
@software{<key>,
  author       = {<Lastname>, <Firstname>},
  title        = {<Repo Title>: <Short description>},
  year         = {<Year>},
  version      = {<vX.Y.Z>},
  url          = {https://github.com/<user>/<repo>},
  note         = {Commit: <short-commit-hash>},
  doi          = {<DOI-if-any>}
}

## 🔒 License

Specify a license (e.g., MIT, Apache‑2.0) here. You can add a `LICENSE` file at the repo root.

## 🙌 Credits
Author: George R. Obaido (and collaborators).  
Contributions welcome via pull requests.
