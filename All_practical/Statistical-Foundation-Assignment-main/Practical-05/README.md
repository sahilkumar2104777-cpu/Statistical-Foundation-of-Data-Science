# Practical 05: Empirical Probabilities on Teaching Ratings and Two-Tailed Z-Test

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Compute empirical probabilities from evaluation scores (`eval`) in the `TeachingRatings.csv` dataset (463 total observations) and perform a two-tailed one-sample z-test using the normal distribution to evaluate whether a sample mean differs from a historical benchmark.

## Files Included
- `Practical5.ipynb.pdf` — Exported Google Colab notebook (`Practical 5.ipynb`) containing code, calculations, and interpretations
- `TeachingRatings.csv` — Dataset used for the probability calculations (loaded in Colab or placed in this folder)

## Questions, Concepts & Methods Covered
- **Q1 — Probability of High Evaluation (`P(eval > 4.5)`):** Counting `79` observations out of `463` with `eval > 4.5` (`probability ≈ 0.1706`, or `17.06%`)
- **Q2 — Interval Probability (`P(3.5 < eval < 4.2)`):** Combining boolean conditions (`(df['eval'] > 3.5) & (df['eval'] < 4.2)`) across `463` observations (`164` matching rows; `probability ≈ 0.3542`, or `35.42%`)
- **Q3 — Two-Tailed Z-Test (`scipy.stats.norm`):** Testing a sample of `n = 36` with sample mean `10.7` against a population mean `mu = 12` and standard deviation `sigma = 5.5` at `alpha = 0.05` (`z ≈ -1.4182`, `p ≈ 0.1561`; since `0.1561 > 0.05`, fail to reject the null hypothesis)

## How to Run / View
1. View `Practical5.ipynb.pdf` directly on GitHub, or open `Practical 5.ipynb` in Google Colab / Jupyter Notebook.
2. Ensure `TeachingRatings.csv` is available at `/content/TeachingRatings.csv` (or update the path if running locally).
3. Run all cells sequentially to reproduce the empirical probabilities and z-test output.
