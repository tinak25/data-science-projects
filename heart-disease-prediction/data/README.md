# Data

`heart.csv` is the heart disease dataset from Kaggle ("Heart Disease Dataset" by johnsmith88), derived from the UCI Heart Disease dataset (Janosi, Steinbrunn, Pfisterer and Detrano, 1988; CC BY 4.0).

| | |
|---|---|
| Rows | 1,025 |
| Unique patients | 302 (723 rows are exact duplicates) |
| Columns | 13 features + `target` (1 = heart disease, 0 = none) |
| Missing values | None |

**Features:** `age`, `sex`, `cp` (chest pain type), `trestbps` (resting blood pressure), `chol` (cholesterol), `fbs` (fasting blood sugar > 120 mg/dl), `restecg` (resting ECG), `thalach` (max heart rate), `exang` (exercise-induced angina), `oldpeak` (ST depression), `slope` (ST slope), `ca` (major vessels coloured by fluoroscopy), `thal` (thalassemia)

## Notes
- Each unique patient appears 3 to 8 times. The notebook shows how this inflates accuracy under a random train/test split.
- A few rows have `ca = 4` or `thal = 0`, which aren't listed in the dataset documentation. They're kept as their own categories.
