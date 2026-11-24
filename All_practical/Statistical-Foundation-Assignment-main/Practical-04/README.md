# Practical 04: Duplicate Handling, Group Comparison, and Multivariate Visualization on Teaching Ratings

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Investigate duplicate instructor observations (`prof`), compare age summary statistics before and after deduplication, evaluate teaching scores across course divisions, and visualize relationships between age, teaching evaluation, gender, and tenure status on the `TeachingRatings.csv` dataset (463 records, 13 columns).

## Files Included
- `Practical4.ipynb.pdf` — Exported Google Colab notebook (`Practical_4_Teaching Ratings.ipynb`) with code, summary outputs, and plots
- `TeachingRatings.csv` — Dataset used for the analysis (loaded in Colab or included in this folder)

## Questions, Concepts & Methods Covered
- **Q1 — Duplicate Professor Records & Age Comparison:**
  - Identifying repeated instructor rows using `df.duplicated(subset=['prof'], keep=False)` (`456` duplicate rows across `94` unique professors)
  - Comparing `age` mean and standard deviation across all `463` course-level observations (`mean = 48.3650`, `SD = 9.8027`) vs. deduplicated instructor-level data (`94` unique professors via `drop_duplicates(subset=['prof'])`: `mean = 47.5532`, `SD = 10.2565`)
- **Q2 — Average Teaching Evaluation by Course Division:** Computing grouped mean `eval` scores (`lower`: `4.0873` vs. `upper`: `3.9526`) and plotting a vertical bar chart (`plt.bar`)
- **Q3 — Age vs. Teaching Evaluation Scatterplot:** Plotting numerical variables `age` and `eval` using `plt.scatter`
- **Q4 — Multivariate Scatterplot by Gender:** Differentiating `male` and `female` observations using `sns.scatterplot(..., hue='gender')`
- **Q5 — Multivariate Scatterplot by Gender and Tenure:** Encoding both `hue='gender'` and `style='tenure'` in `sns.scatterplot` to compare evaluation trends across demographic and tenure groups

## How to Run / View
1. View `Practical4.ipynb.pdf` directly on GitHub, or open `Practical_4_Teaching Ratings.ipynb` in Google Colab / Jupyter Notebook.
2. Ensure `TeachingRatings.csv` is available at `/content/TeachingRatings.csv` (or update the CSV path if running locally).
3. Run all cells sequentially to reproduce the deduplication analysis, summary statistics, and Matplotlib/Seaborn plots.
