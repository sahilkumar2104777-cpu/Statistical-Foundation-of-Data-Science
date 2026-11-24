# Practical 06: Two-Sample T-Test, One-Way ANOVA, Chi-Square Test, and Pearson Correlation on Teaching Ratings

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Apply inferential statistical tests and correlation analysis to `TeachingRatings.csv` (`463` rows, `13` columns) to evaluate differences in teaching evaluation scores by gender, differences in beauty scores across age groups, association between tenure and gender, and linear correlation between beauty and teaching evaluation scores[cite: 39].

## Files Included
- `Practical6.ipynb.pdf` — Exported Google Colab notebook (`Practical 6.ipynb`) containing hypotheses, code, outputs, and conclusions[cite: 39]
- `TeachingRatings.csv` — Dataset used for the analysis (loaded via `/content/TeachingRatings.csv` in Colab or placed in this folder)[cite: 39]

## Questions, Concepts & Methods Covered
- **Q1 — Independent Two-Sample T-Test (`scipy.stats.ttest_ind(..., equal_var=True)`):** Testing whether `eval` differs between `female` and `male` instructors at `alpha = 0.05` (`T-statistic ≈ -3.2499`, `P-value ≈ 0.00124`; since `0.00124 < 0.05`, reject `H0`)[cite: 39, 40, 41]
- **Q2 — One-Way ANOVA (`scipy.stats.f_oneway`):** Grouping `age` into three categories (`<= 40`, `> 40 and < 57`, and `>= 57`) and testing whether mean `beauty` scores differ across age groups (`F-statistic ≈ 17.5976`, `P-value ≈ 4.32e-08`; reject `H0`)[cite: 41, 42]
- **Q3 — Chi-Square Test of Independence (`scipy.stats.chi2_contingency`):** Evaluating association between categorical `tenure` (`yes`/`no`) and `gender` (`female`/`male`) from a contingency table (`Chi-square ≈ 2.2068`, `P-value ≈ 0.1374`, `dof = 1`; since `0.1374 > 0.05`, fail to reject `H0`)[cite: 42, 43]
- **Q4 — Pearson Correlation (`scipy.stats.pearsonr`):** Measuring linear correlation between `beauty` and `eval` (`Correlation coefficient r ≈ 0.1890`, `P-value ≈ 4.25e-05`; reject `H0`, indicating a statistically significant but weak positive correlation)[cite: 43]

## How to Run / View
1. View `Practical6.ipynb.pdf` directly in this folder on GitHub, or open `Practical 6.ipynb` in Google Colab / Jupyter Notebook
2. Ensure `TeachingRatings.csv` is accessible at `/content/TeachingRatings.csv` (or update the file path if running locally)
3. Run all cells sequentially to reproduce the t-test, ANOVA, Chi-square, and Pearson correlation results
