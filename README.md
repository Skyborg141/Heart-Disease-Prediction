# ❤️ Heart Disease Prediction

> A supervised machine learning project that predicts the presence of heart disease in patients using clinical data from the **UCI Cleveland Heart Disease Dataset**. The project covers the complete ML pipeline — from exploratory data analysis and preprocessing to model training, evaluation, and comparison.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Project Workflow](#project-workflow)
- [Models Used](#models-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Key Insights](#key-insights)
- [Disclaimer](#disclaimer)

---

## Overview

Heart disease is one of the leading causes of death worldwide. Early and accurate prediction using patient clinical data can significantly aid medical professionals in diagnosis and prevention. This project builds and compares classification models on the UCI Heart Disease dataset to predict whether a patient has heart disease (binary classification: **1 = disease present**, **0 = no disease**).

---

## Dataset

| Property | Details |
|----------|---------|
| **File** | `heart.csv` |
| **Source** | UCI Machine Learning Repository — Cleveland Heart Disease Dataset |
| **Samples** | 303 patients |
| **Features** | 13 clinical input features |
| **Target** | `target` — binary (1 = heart disease, 0 = no heart disease) |
| **Missing values** | None (clean dataset) |
| **Class distribution** | Approximately balanced (~54% positive, ~46% negative) |

---

## Features

| Feature | Type | Description |
|---------|------|-------------|
| `age` | Continuous | Age of the patient in years |
| `sex` | Categorical | Sex (1 = male, 0 = female) |
| `cp` | Categorical | Chest pain type (0 = typical angina, 1 = atypical angina, 2 = non-anginal pain, 3 = asymptomatic) |
| `trestbps` | Continuous | Resting blood pressure (mm Hg on hospital admission) |
| `chol` | Continuous | Serum cholesterol in mg/dl |
| `fbs` | Categorical | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| `restecg` | Categorical | Resting ECG results (0 = normal, 1 = ST-T wave abnormality, 2 = left ventricular hypertrophy) |
| `thalach` | Continuous | Maximum heart rate achieved |
| `exang` | Categorical | Exercise-induced angina (1 = yes, 0 = no) |
| `oldpeak` | Continuous | ST depression induced by exercise relative to rest |
| `slope` | Categorical | Slope of the peak exercise ST segment (0 = upsloping, 1 = flat, 2 = downsloping) |
| `ca` | Categorical | Number of major vessels colored by fluoroscopy (0–3) |
| `thal` | Categorical | Thalassemia (0 = normal, 1 = fixed defect, 2 = reversible defect) |
| `target` | Binary | **Target variable** — presence of heart disease (1 = yes, 0 = no) |

---

## Project Workflow

```
heart.csv
    │
    ▼
1. Data Loading & Inspection
   └── Shape, dtypes, null check, value counts
    │
    ▼
2. Exploratory Data Analysis (EDA)
   ├── Distribution of each feature
   ├── Target class balance
   ├── Correlation heatmap
   └── Feature vs. target visualizations
    │
    ▼
3. Data Preprocessing
   ├── Encoding categorical variables
   ├── Feature scaling (StandardScaler / MinMaxScaler)
   └── Train-test split (typically 80/20)
    │
    ▼
4. Model Training
   └── Multiple classifiers trained and compared
    │
    ▼
5. Model Evaluation
   ├── Accuracy, Precision, Recall, F1-Score
   ├── Confusion Matrix
   └── ROC-AUC Curve
    │
    ▼
6. Best Model Selection & Prediction
```

---

## Models Used

> ⚠️ **Note:** The notebook (4.88 MB) is too large to render on GitHub. The specific models and their exact accuracy scores from this notebook are listed below — update this section with your actual results.

Common classifiers used in this type of project:

| Model | Description |
|-------|-------------|
| Logistic Regression | Linear baseline classifier for binary outcomes |
| K-Nearest Neighbors (KNN) | Distance-based non-parametric classifier |
| Decision Tree | Rule-based tree structure for classification |
| Random Forest | Ensemble of decision trees (bagging) |
| Support Vector Machine (SVM) | Finds optimal hyperplane between classes |
| Naive Bayes | Probabilistic classifier based on Bayes' theorem |

**→ Replace this table with your actual models and accuracy scores from the notebook.**

---

## Evaluation Metrics

The models are evaluated using the following metrics:

- **Accuracy** — overall percentage of correct predictions
- **Precision** — of all predicted positives, how many were actually positive
- **Recall (Sensitivity)** — of all actual positives, how many were correctly identified
- **F1-Score** — harmonic mean of precision and recall
- **Confusion Matrix** — breakdown of TP, TN, FP, FN
- **ROC-AUC** — area under the Receiver Operating Characteristic curve

In medical classification tasks, **Recall** is particularly important — minimizing false negatives (missed disease cases) is critical.

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| `Python 3` | Core language |
| `Jupyter Notebook` | Interactive development environment |
| `pandas` | Data loading, manipulation, and exploration |
| `NumPy` | Numerical operations |
| `Matplotlib` | Data visualization |
| `Seaborn` | Statistical visualizations (heatmaps, distribution plots) |
| `scikit-learn` | ML models, preprocessing, train-test split, metrics |

---

## Getting Started

### Prerequisites

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### Run the Notebook

```bash
# 1. Clone the repository
git clone https://github.com/Skyborg141/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction

# 2. Launch Jupyter
jupyter notebook Heart_Disease_Prediction.ipynb
```

Or open directly in **Google Colab**:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Skyborg141/Heart-Disease-Prediction/blob/main/Heart_Disease_Prediction.ipynb)

---

## Project Structure

```
Heart-Disease-Prediction/
│
├── Heart_Disease_Prediction.ipynb   # Main notebook — full ML pipeline
├── heart.csv                        # UCI Cleveland dataset (303 samples, 14 columns)
└── .gitattributes
```

---

## Key Insights

Based on well-known analysis of the UCI Cleveland dataset:

- **`cp` (chest pain type)**, **`thalach` (max heart rate)**, and **`slope`** show strong **positive correlation** with heart disease presence
- **`ca` (vessels colored)**, **`thal`**, **`exang`**, and **`oldpeak`** show strong **negative correlation** with the target
- **`fbs`**, **`chol`**, and **`restecg`** have relatively low predictive power individually
- Patients with **asymptomatic chest pain (cp = 3)** are paradoxically more likely to have heart disease in this dataset

> ⚠️ Update this section with the specific findings and accuracy results from your notebook.

---

## Disclaimer

This project is for **educational and research purposes only**. The predictions made by these models should **not** be used as a substitute for professional medical advice, diagnosis, or treatment.

---

## License

No license file is included in this repository.
