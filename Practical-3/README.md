# Student Rating Dataset – Practical Report

## 1. Percentage of Visible Minority Professors Who Are Tenured

### Python Code

```python
import pandas as pd

df = pd.read_csv("TeachingRatings.csv")

minority_tenure = pd.crosstab(
    df["minority"],
    df["tenure"],
    normalize="index"
) * 100

print(minority_tenure)
```

### Result

```text
tenure       no    yes
minority              
no        23.06  76.94
yes       15.62  84.38
```

### Interpretation

This table gives the percentage of tenured and untenured professors within each minority group. Comparing the percentages helps determine whether tenure status differs between visible-minority and non-minority professors.

---

## 2. Does Average Age Differ by Tenure?

### Python Code

```python
age_stats = df.groupby("tenure")["age"].agg(["mean", "std"])

print(age_stats)
```

### Result

```text
         mean    std
tenure              
no      50.19   6.95
yes     47.85  10.42
```

### Interpretation

The mean is the average age. The standard deviation shows how much the ages vary around the average.

---

## 3. Best Graph for the Age Variable

A **histogram** works well for age because age is numerical data. It shows how professors are distributed across different age ranges.

### Python Code

```python
import matplotlib.pyplot as plt

plt.hist(df["age"].dropna(), bins=10, edgecolor="black")
plt.xlabel("Age")
plt.ylabel("Number of Professors")
plt.title("Distribution of Professor Ages")
plt.show()
```

**Generated graph:** `age_distribution.png`

---

## 4. Difference Between `pyplot.bar()` and `pyplot.barh()`

- `plt.bar()` creates a **vertical** bar chart.
- `plt.barh()` creates a **horizontal** bar chart.

### Comparison

| Function | Direction |
|---|---|
| `plt.bar()` | Vertical |
| `plt.barh()` | Horizontal |

### Gender Graph Code

```python
gender_counts = df["gender"].value_counts()

plt.bar(gender_counts.index, gender_counts.values)
plt.xlabel("Gender")
plt.ylabel("Number of Professors")
plt.title("Number of Professors by Gender")
plt.show()
```



---

## 5. Median Evaluation Score for Tenured Professors

### Python Code

```python
median_eval = df.loc[df["tenure"] == 1, "eval"].median()

print(median_eval)
```

### Result

**Median evaluation score for tenured professors: nan**

---

# Conclusion

This practical demonstrates:

- Crosstab and percentage calculation
- `groupby()`
- Mean and standard deviation
- Histograms
- Vertical and horizontal bar charts
- Median calculation
- Filtering data using tenure status


