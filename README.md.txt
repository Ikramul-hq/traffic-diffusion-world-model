# Generative Traffic Forecasting with Diffusion World Models

This repository contains the implementation of a **Conditional Diffusion Model** for spatiotemporal traffic forecasting. Unlike standard regression baselines (e.g., STGCN, LSTM) which smooth out congestion patterns, this model uses a generative approach to preserve the sharp shockwave structures of real-world traffic jams.

## 📊 Results

### 1. Shockwave Preservation
The model captures the sharp gradients of traffic congestion that are often lost in regression-based approaches.
![Single Forecast](results/fig1_forecast_sharp.png)

### 2. Spatiotemporal Dynamics (1-Hour Rollout)
Autoregressive generation over a 1-hour horizon demonstrates temporal stability and the propagation of phantom traffic jams.
![Heatmap](results/fig2_heatmap.png)

### 3. Quantitative Error
The model achieves an MAE of ~5.32 mph (Ensemble) / ~4.0 mph (History-Aware) on the PeMSD7 dataset.
![Error Dist](results/fig3_error_sharp.png)

## 🚀 Usage

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt