# Task 4
# Classification with Logistic Regression.
---

## Dataset

- **Source:** https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data.
- **Features:** 30 numeric features computed from a digitized image of a breast mass.
- **Target:** `diagnosis` - Malignant (M) or Benign (B)

---

## Steps Performed

### 1. Load Dataset

- Loaded `data.csv` into a pandas DataFrame.
- Inspected structure and verified class labels.

### 2. Data Preprocessing
- Displayed summary statistics using `describe()`.
- Dropped unnecessary columns (`id`,`Unnamed: 23`).
- Converted `diagnosis`:
  - 'M' → 1 (Malignant)
  - 'B' → 0 (Benign)
- Split data into training and testing sets (80/20).
- Scaled features using `StandardScaler`.

### 3. Logistic Regression Model

- Trained a `LogisticRegression()` model on scaled data.
- Obtained predictions and probability scores.

### 4. Evaluation Metrics

- Confusion Matrix
- Precision, Recall, F1-Score
- ROC-AUC Score
- ROC Curve plotted using `roc_curve()`

### 5. Threshold Tuning

- Adjusted decision threshold from 0.5 to 0.3.
- Recomputed confusion matrix and classification report.
- Explained **sigmoid function** used for probability output:
  σ(z)= 1/(
1+e^−z)
​


---

## Key Results

- **High ROC-AUC score** indicates strong classifier performance.
- **Tuning the threshold** improved recall at the cost of precision.
