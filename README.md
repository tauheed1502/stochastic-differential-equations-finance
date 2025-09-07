# Stochastic Differential Equations for Financial Time Series  

## 📌 Overview  
This project explores the application of **Stochastic Differential Equations (SDEs)** to model stock price dynamics and volatility in financial markets. Both **classical SDEs** (Geometric Brownian Motion, Ornstein–Uhlenbeck, Heston) and **Neural SDEs** are implemented and benchmarked against traditional econometric models such as **GARCH/ARCH**.  

The goal is to evaluate the ability of SDE-based models to capture the statistical properties of high-frequency intraday NSE data, generate realistic synthetic trajectories, and improve forecasting accuracy.  

---

## 🚀 Key Features  
- **Classical SDE Implementations**  
  - Geometric Brownian Motion (GBM)  
  - Ornstein–Uhlenbeck (OU) Process  
  - Heston Stochastic Volatility Model  
- **Parameter Estimation**  
  - Maximum Likelihood Estimation (MLE)  
  - Kalman Filtering for latent volatility states  
- **Simulation**  
  - Monte Carlo (~100k trajectories) with Euler–Maruyama & Milstein schemes  
  - Validation of synthetic paths against empirical moments  
- **Neural SDEs (via `torchsde`)**  
  - Learned dynamics from data  
  - ~18% improvement in log-likelihood over classical SDEs  
  - Outperformed GARCH/ARCH benchmarks on intraday returns  
- **Robust Validation**  
  - Distributional consistency checks  
  - Backtesting with realized volatility measures  

---

## 📂 Project Structure  
```bash
stochastic-differential-equations-finance/
│
├── data/              # Raw, processed, and synthetic data
├── models/            # Classical & Neural SDE model implementations
├── src/               # Estimation, simulation, validation, utilities
├── notebooks/         # Jupyter notebooks for experiments
├── results/           # Model outputs, figures, metrics
├── tests/             # Unit tests
├── config/            # Config files
├── docs/              # Documentation and methodology notes
├── README.md          # Project documentation
├── requirements.txt   # Dependencies
├── setup.py           # Setup script
└── .gitignore
