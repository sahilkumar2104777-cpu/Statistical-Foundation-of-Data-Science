# Practical 02: Exploratory Data Analysis, Hypothesis Testing, and Chi-Square Analysis on Teaching Ratings

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Explore the `TeachingRatings.csv` dataset (463 observations across 13 variables) by classifying data type, computing descriptive statistics, visualizing distributions and skewness, testing mean beauty score differences across gender, and analyzing tenure proportions by gender using a chi-square test.

## Files Included
- `Practical2.ipynb.pdf` — Exported Google Colab notebook (`Assignment2.ipynb`) containing code, outputs, and plots
- `TeachingRatings.csv` — Dataset used for the analysis (if uploaded in this folder or loaded via Google Drive)

## Key Questions & Statistical Methods Covered
- **Q1 — Data Classification:** Identifying `TeachingRatings.csv` as cross-sectional data (463 course/instructor records) rather than time-series data
- **Q2 & Q3 — Descriptive Statistics:** Calculating mean (`36.62`), median (`23.0`), minimum (`5`), and maximum (`380`) for `students`, along with summary statistics via `df.describe()`, `df.info()`, and `df.shape` (`(463, 13)`)
- **Q4 — Distribution & Skewness:** Plotting a 15-bin histogram of `beauty` scores and computing skewness (`~0.5158`)
- **Q5 — Two-Sample Welch's t-Test:** Comparing `beauty` scores across `gender` (`female`: `195`, mean `0.1161`; `male`: `268`, mean `-0.0845`) using `scipy.stats.ttest_ind(..., equal_var=False)` (`t ≈ -2.6880`, `p ≈ 0.0075`)
- **Q6 — Contingency Table & Chi-Square Test:** Computing row-normalized tenure percentages by gender (`female`: `74.36%` tenured; `male`: `80.60%` tenured) and running `scipy.stats.chi2_contingency` (`chi2 ≈ 2.2068`, `p ≈ 0.1374`, `dof = 1`)

## How to Run / View
1. View `Practical2.ipynb.pdf` directly in this folder on GitHub, or open the corresponding notebook in Google Colab / Jupyter Notebook.
2. Update the file path for `TeachingRatings.csv` if running locally instead of from `/content/drive/MyDrive/TeachingRatings.csv`.
3. Run all cells sequentially to reproduce the statistics, histogram, t-test, and chi-square results.
