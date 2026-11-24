# Practical 09: K-Nearest Neighbors (KNN) Classification on the Iris Dataset[cite: 60, 62]

## Student Information
- **Name:** Ankush Kumar Singh
- **Registration Number:** GF202459590
- **Subject:** Statistical Foundation of Data Science

## Objective
Perform exploratory data analysis (EDA) on the scikit-learn Iris dataset (`150` samples across `3` species: `setosa`, `versicolor`, and `virginica`), tune the number of neighbors (`K` from `1` to `20`) using `StandardScaler` inside a leakage-free `Pipeline` with 5-fold stratified cross-validation, and evaluate the final KNN classifier on a held-out `20%` test set

## Files Included
- `Practical_9_KNN_Iris_Dataset.ipynb - Colab.pdf` — Exported Google Colab notebook containing EDA, cross-validation results, error-rate plot, confusion matrix, classification report, and test scatter plot

## Steps, Concepts & Methods Covered
- **EDA & Stratified Train-Test Split:** Exploring `150` records (`4` measurement features: `sepal length (cm)`, `sepal width (cm)`, `petal length (cm)`, `petal width (cm)`), `50` records per species, and `0` missing values[cite: 60, 61], followed by an `80/20` stratified split (`120` training samples, `30` test samples) with `random_state=42`
- **Feature Scaling & Cross-Validation (`K = 1` to `20`):** Using `StandardScaler` + `KNeighborsClassifier` inside a `Pipeline` with `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`[cite: 60, 61], selecting `K = 3` (`Mean CV Accuracy = 0.9667`, `Mean CV Error Rate = 0.0333`) and plotting error rate vs. `K`
- **Final Model Evaluation & Visualization:** Fitting the `K = 3` pipeline on the full training set and evaluating on the `30` test samples (`Test Accuracy = 0.9333` / `93.33%`, `Test Error Rate = 0.0667` / `6.67%`), inspecting the confusion matrix (`[[10, 0, 0], [0, 10, 0], [0, 2, 8]]`), classification report, and a test scatter plot of `sepal length (cm)` vs. `petal length (cm)` colored by actual species and marked by prediction correctness

## How to Run / View
1. View `Practical_9_KNN_Iris_Dataset.ipynb - Colab.pdf` directly in this folder on GitHub, or open the notebook in Google Colab / Jupyter Notebook.
2. No external CSV download is required because the dataset is loaded via `sklearn.datasets.load_iris(as_frame=True)`.
3. Run all cells sequentially from Step 1 to Step 9 to reproduce the tables, cross-validation curve, confusion matrix, and scatter plot
