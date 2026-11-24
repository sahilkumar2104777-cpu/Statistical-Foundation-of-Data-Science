# Practical 07: Regression Analysis — T-Test, ANOVA, and Correlation via OLS on Teaching Ratings

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Apply Ordinary Least Squares (OLS) regression using `statsmodels` on the `TeachingRatings.csv` dataset (`463` rows, `13` columns) to examine how regression models connect to a t-test for gender differences in teaching evaluations, a one-way ANOVA for beauty score differences across age groups, and simple linear regression for the relationship between beauty and teaching evaluation scores

## Files Included
- `Practical7.ipynb.pdf` — Exported Google Colab notebook (`Practical_7_Teaching Ratings_Regression.ipynb`) containing code, OLS summaries, ANOVA tables, regression plots, and interpretations
- `TeachingRatings.csv` — Dataset used for the analysis (loaded via `/content/TeachingRatings.csv` in Colab or placed in this folder)

## Questions, Concepts & Methods Covered
- **Q1 — Regression with T-Test (`smf.ols('eval ~ female', data=df)`):** Using a binary `female` indicator (`1` for female, `0` for male) to test whether gender affects teaching evaluation scores (`eval`), noting a statistically significant difference at `p < 0.05` (`female` coefficient `≈ -0.1680`, `t ≈ -3.250`, `p ≈ 0.001`, `R-squared ≈ 0.022`)
- **Q2 — Regression with ANOVA (`smf.ols('beauty ~ C(age_group)', data=df)` + `anova_lm(..., typ=2)`):** Grouping `age` into three categories (`<= 40`, `between 40 and 57 years`, and `>= 57`) and testing whether mean `beauty` scores differ across age groups (`p < 0.05`, rejecting `H0` for a statistically significant difference across age groups)
- **Q3 — Correlation Using Regression (`smf.ols('eval ~ beauty', data=df)` + `sns.regplot`):** Fitting a simple OLS regression of `eval` on `beauty` and plotting the regression line (`Intercept = 3.9983`, `beauty` coefficient `= 0.1330`, `t = 4.133`, `p = 4.25e-05`, `R-squared = 0.036`, explaining about `3.6%` of variation in evaluation scores)

## How to Run / View
1. View `Practical7.ipynb.pdf` directly in this folder on GitHub, or open `Practical_7_Teaching Ratings_Regression.ipynb` in Google Colab / Jupyter Notebook
2. Ensure `TeachingRatings.csv` is available at `/content/TeachingRatings.csv` (or update `file_path` if running locally)
3. Run all cells sequentially to reproduce the OLS summaries, ANOVA output, and regression plot
