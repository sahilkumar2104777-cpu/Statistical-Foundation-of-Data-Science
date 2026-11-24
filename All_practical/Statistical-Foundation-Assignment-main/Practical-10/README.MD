# Practical 10: Principal Component Analysis (PCA) on the Wine Dataset

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Explore the scikit-learn Wine dataset (`178` samples, `13` chemical features, `3` wine classes: `class_0`, `class_1`, and `class_2`), inspect feature distributions and covariance, standardize features using `StandardScaler`, and apply Principal Component Analysis (`PCA(n_components=2)`) to visualize class separation in the first two principal components
## Files Included
- `Practical_10_PCA_Wine_Dataset.ipynb - Colab.pdf` — Exported Google Colab notebook containing summary statistics, boxplots, scatter plot, covariance matrix heatmap, standardized scaling check, and 2D PCA projection

## Steps, Concepts & Methods Covered
- **Dataset Loading & Descriptive Statistics:** Loading `load_wine()` (`178` rows, `13` features) and inspecting summary statistics (`mean`, `std`, `min`, quartiles, `max`) across features with different scales (such as `proline` vs. `nonflavanoid_phenols`).
- **Class Boxplots & Two-Feature Scatterplot:** Comparing `alcohol`, `malic_acid`, `color_intensity`, and `proline` across wine classes using boxplots, and plotting `alcohol` vs. `color_intensity` colored by `class`
- **Covariance Matrix (`X.cov()`):** Computing and visualizing the `13 x 13` covariance matrix heatmap, noting how scale differences affect covariance magnitude.
- **Feature Scaling & 2D PCA (`PCA(n_components=2)`):** Standardizing features to mean `0` and standard deviation `1` via `StandardScaler`, projecting onto `PC1` (`36.20%` explained variance) and `PC2` (`19.21%` explained variance; `55.41%` combined variance), and plotting the three wine classes in principal component space

## How to Run / View
1. View `Practical_10_PCA_Wine_Dataset.ipynb - Colab.pdf` directly in this folder on GitHub, or open the notebook in Google Colab / Jupyter Notebook.
2. No external CSV download is required because the dataset is loaded via `sklearn.datasets.load_wine()`
3. Run all cells sequentially from Step 1 to Step 7 to reproduce the tables, boxplots, scatter plots, covariance heatmap, and PCA projection
