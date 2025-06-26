# Goldman Sachs India Hackathon (Quant) 2025 Project

A modular quantitative finance project developed for the Goldman Sachs India Hackathon 2025, implementing key models in risk management, market making, and exotic derivatives pricing.

---

## 📌 Modules

### 1. Optimal Hedging Strategy

Constructs a hedge portfolio that minimizes 95% Value-at-Risk (VaR) under capital cost constraints.

- Models used:
  - Lasso Regression
  - Quantile Regression
  - LightGBM Regressor (Quantile objective)

- Data:
  - Historical stock returns
  - Cost, sector, rating, and market cap metadata

---

### 2. Automated Market Making

Implements a market-making agent that dynamically adjusts bid–ask quotes to balance spread capture and inventory risk.

- Framework:
  - Avellaneda–Stoikov quoting model

- Controls:
  - Inventory-aware pricing
  - Trade pressure skew
  - Order Flow Imbalance (OFI)

---

### 3. Exotic Option Pricing

Prices knock-out basket options on correlated stocks using a calibrated local volatility model.

- Calibration:
  - Dupire local volatility surface inferred by inverting Black–Scholes prices
  - Newton–Raphson optimization to match market quotes

- Pricing:
  - Monte Carlo simulation
  - Correlated Brownian motion to model asset dynamics
  - Early knockout logic embedded in simulation

---

## 🛠 Tech Stack

- Python (NumPy, pandas, SciPy)
- scikit-learn, LightGBM, PyTorch
- Matplotlib / Seaborn for plots
- Jupyter Notebooks for development

---

## 🔧 Improvements

These were explored beyond the core implementation:

- Feature engineering with metadata (rating, sector, market cap)
- Rolling-window retraining for hedging model
- Use of Order Flow Imbalance (OFI) and trade pressure for real-time quote skew
- Optimization techniques in Monte Carlo pricing

---

