# Practical 11: Sunspot Numbers — Gamma Model and Metropolis-Hastings MCMC[cite: 39]

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Analyze the monthly mean total sunspot number dataset (`SN_m_tot_V2.0.csv`, filtered to `decimal_date <= 2018.874`, `3,239` rows and `7` columns) to observe solar cycle oscillations, fit a Gamma distribution to positive right-skewed sunspot counts, and estimate Gamma shape (`a`) and scale (`b`) parameters via Metropolis-Hastings MCMC across three data subsets[cite: 39, 40, 42].

## Files Included
- `Practical11.pdf` — Exported Google Colab notebook (`Practical 11 - Sunspot Numbers: Gamma Model + MCMC (Metropolis)`) containing code, plots, MCMC diagnostics, posterior summaries, and conclusions
- `SN_m_tot_V2.0.csv` — Sunspot dataset used in the notebook (loaded from `/content/SN_m_tot_V2.0.csv` in Colab)

## Steps, Concepts & Methods Covered
- **Time-Series & 12-Year Cycle Exploration:** Plotting monthly sunspot numbers across `1749–2018` (`~11-year` solar cycle oscillation with varying peak heights) and overlaying 12-year cycles (`cycle` and `t_in_cycle`) alongside the mean profile
- **Gamma MLE Fit on Positive Counts:** Dropping zero values (`67` zeros dropped where `sunspot <= 0`) and fitting a Gamma distribution (`stats.gamma.fit(x_pos, floc=0)`) over the histogram of positive sunspot counts (`a ≈ 1.17`, `b ≈ 71.6`)
- **Metropolis-Hastings MCMC (`10,000` iterations, `burn = 2000`):** Starting from `a = 4, b = 10` with flat priors on `a, b > 0`, running the sampler on `First 50 samples` (`a ≈ 6.19`, `b ≈ 18.15`, implied mean `107.41`), `All samples` (`a ≈ 1.18`, `b ≈ 71.40`, implied mean `84.05`), and `Last 50 samples` (`a ≈ 1.31`, `b ≈ 32.36`, implied mean `41.05`)
- **Posterior Diagnostics & Group Comparison:** Inspecting trace plots and post-burn-in histograms, computing posterior means and `95%` credible intervals (`2.5%` to `97.5%` percentiles), and comparing fitted Gamma curves against each group's data

## How to Run / View
1. View `Practical11.pdf` directly in this folder on GitHub, or open the notebook in Google Colab / Jupyter Notebook
2. Ensure `SN_m_tot_V2.0.csv` is available at `/content/SN_m_tot_V2.0.csv` (or update the path if running locally)
3. Run all cells sequentially from Step 1 to Step 6 to reproduce the time-series plots, MLE fit, MCMC traces, posterior summary table, and group comparison plots
