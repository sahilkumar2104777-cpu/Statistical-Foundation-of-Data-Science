# Practical 03: Teaching Ratings — Tenure, Age, Gender, and Evaluation Analysis

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Analyze instructor characteristics (`minority`, `tenure`, `age`, `gender`) and teaching evaluation scores (`eval`) on the University of Texas at Austin `TeachingRatings` dataset (463 records, 2000–2002) using cross-tabulation, a Chi-square test of independence, group summary statistics, histograms, bar charts, and median evaluation analysis.

## Files Included
- `Practical3.ipynb.pdf` — Exported Google Colab notebook (`Practical_3_Teaching Ratings.ipynb`) with explanations, code, tables, and charts
- `TeachingRatings.csv` — Dataset used for the practical (loaded via Google Drive or included in this folder)

## Questions, Concepts & Methods Covered
- **Q1 — Tenure Status by Minority Status:** Row-normalized cross-tabulation (`pd.crosstab(..., normalize='index') * 100`) showing `84.38%` of visible-minority (`minority == 'yes'`) instructors are on the tenure track (`tenure == 'yes'`), followed by a Chi-square test of independence (`chi2 = 1.3675`, `p = 0.2422`, `dof = 1` at the 5% significance level: insufficient evidence of a significant association)
- **Q2 — Age Comparison by Tenure:** Grouped mean and standard deviation of `age` by `tenure` (`tenure == 'no'`: mean `50.186`, std `6.946`; `tenure == 'yes'`: mean `47.850`, std `10.420`)
- **Q3 — Visualizing Numerical Age (`plt.hist`):** Using a 10-bin histogram for the quantitative `age` variable rather than a bar chart
- **Q4 — Categorical Gender Visualization (`plt.bar` vs. `plt.barh`):** Comparing vertical bar charts (`plt.bar`) and horizontal bar charts (`plt.barh`), and plotting instructor counts by `gender` (`male`: `268`, `female`: `195`)
- **Q5 — Median Evaluation Score for Tenure-Track Instructors:** Filtering `tenure == 'yes'` and computing the median `eval` score (`4.00`)

## How to Run / View
1. View `Practical3.ipynb.pdf` directly on GitHub, or open `Practical_3_Teaching Ratings.ipynb` in Google Colab / Jupyter Notebook.
2. Mount Google Drive or adjust the path to `TeachingRatings.csv` if running outside Colab.
3. Run all cells sequentially to reproduce the cross-tabs, Chi-square output, group summaries, and plots.
