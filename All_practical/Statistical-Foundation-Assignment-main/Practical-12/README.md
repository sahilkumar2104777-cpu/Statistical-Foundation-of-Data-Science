# Practical 12: Metropolis Algorithm and Deterministic Logistic Growth Model

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective[cite: 43, 45, 47, 49].

## Files Included
- `Practical12.pdf` — Exported notebook (`Practical12.html`) containing Part A (Metropolis Algorithm) and Part B (Deterministic Logistic Growth Model), code, outputs, plots, and conclusions
## Parts, Concepts & Methods Covered
- **Part A — Metropolis Algorithm (`scipy.stats.norm`):** Generating `1,000` iterations starting at `initial_value = 0` with `proposal_std = 1` (`acceptance rate ≈ 0.6992`) to sample from a standard normal distribution (`loc=0, scale=1`), and comparing the sample histogram against the theoretical normal PDF curve
- **Part B — Deterministic Logistic Growth Model (Euler's Method):** Simulating population growth over `200` time steps from `t = 0` to `50` with `r = 0.2`, `K = 1000`, and `P0 = 50` using Euler's Method (`final population ≈ 999.22`), and plotting the S-shaped growth trajectory relative to carrying capacity `K`

## How to Run / View
1. View `Practical12.pdf` directly in this folder on GitHub, or open the corresponding script/notebook in your Python environment (such as Jupyter Notebook or Google Colab).
2. No external CSV dataset is required; both simulations generate data programmatically using `numpy`, `matplotlib`, and `scipy`
3. Run the cells for Part A and Part B sequentially to reproduce the sample outputs, acceptance rate, normal density overlay, population values, and logistic growth curve
