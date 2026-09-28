

# NumPy Mastery

A complete, hands-on NumPy tutorial series — 340+ executed code cells covering everything from array basics to broadcasting, structured arrays, linear algebra, and statistics. Built with real, runnable Jupyter notebooks, not just theory.

## What's covered

| Notebook | Topics |
|---|---|
| `01_numpy_basics.ipynb` | Arrays, dtypes, ufuncs, broadcasting, memory layout, complex numbers |
| `02_array_creation.ipynb` | zeros/ones/arange/linspace, structured arrays, datetime64, random generation, saving/loading |
| `03_indexing_slicing.ipynb` | Boolean/fancy indexing, `take`/`put`, structured array indexing |
| `04_reshaping_stacking.ipynb` | reshape, stack/split, moveaxis, padding, kron/outer products |
| `05_searching_sorting_filtering.ipynb` | sorting, `where`, set operations, `linalg`, polynomial fitting, statistics |
| `stock_movement_predictor.ipynb` | Feature engineering, walk-forward validation, AAPL next-day direction classifier |

## Stock Movement Predictor — AAPL Next-Day Direction

Project idea #3 from the board. Predicts whether AAPL closes up or down the next trading day, using engineered technical features and a classifier — evaluated with real rigor, not just a headline accuracy number.

### The honest result (this is the point of the project)

| Approach | Accuracy |
|---|---|
| **Naive "always up"** | **52.6%** |
| Logistic Regression | 52.0% |
| Random Forest | 52.0% |
| Persistence (same as yesterday) | 50.5% |
| Gradient Boosting | 50.2% |

**The naive baseline beat every trained model.** Walk-forward validation across 5 time windows confirms this — the model only beat the baseline in 2 of 5 folds.

This is not a failed project — it's an honest, correctly-executed demonstration that AAPL's next-day direction is very close to a coin flip once you control for the natural upward drift of stocks over time. A project that claimed 70%+ accuracy on this exact task would almost certainly have a data leakage bug, not a real edge.

### What's in here

| File | What it is |
|---|---|
| `stock_movement_predictor.ipynb` | The full notebook — 49 cells, feature engineering through walk-forward validation |
| `data/aapl_1980_2024.csv` | Real daily AAPL price data, 1980-2024 (11,084 trading days) |

### Data source

Yahoo Finance's live API (`yfinance`) is blocked in the sandboxed environment this was built in, so a static historical CSV (sourced from Yahoo Finance data, mirrored on GitHub) was used instead. If you have normal internet access, you can swap in live `yfinance` calls with no other code changes — the feature engineering and modeling logic is identical either way.

### What real rigor looks like here

- **Two real baselines** (naive-always-up, persistence) that the model must beat to mean anything
- **Strict chronological train/test split** — no shuffling, no future-leaking into training
- **Walk-forward validation** across 5 sequential time windows, not one lucky split
- **Honest reporting** of a negative result, with an explanation of why that's the expected, correct outcome

### Why this still matters for a portfolio

Anyone with ML experience reading this notebook will recognize the rigor (proper time splits, real baselines, walk-forward testing) as the mark of someone who understands evaluation — which is a stronger signal than an inflated accuracy number that wouldn't survive scrutiny.

## Who this is for

Anyone learning NumPy from scratch or wanting a reference with runnable, real-world-flavored examples rather than toy `[1,2,3]` arrays everywhere.

## Requirements

```bash
pip install numpy jupyter pandas scikit-learn matplotlib seaborn
```

## Author

[Preetham](https://github.com/preetamvr1595) — MCA student, building a complete data science learning path from the ground up

<!-- Last updated: 2026-09-28 -->
