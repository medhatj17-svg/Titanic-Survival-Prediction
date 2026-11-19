# 🚢 Titanic Survival Prediction — Machine Learning

A Machine Learning classification project that predicts whether a passenger survived the Titanic disaster using passenger information and classification algorithms.

## 📌 Project Overview

This project aims to predict passenger survival on the Titanic dataset by implementing and comparing two Machine Learning classification models:

- Random Forest Classifier
- Support Vector Machine (SVM)

The project includes data exploration, feature engineering, preprocessing, hyperparameter tuning, model evaluation, and final predictions for the official Kaggle test dataset.

## 📊 Dataset

The project uses the **Titanic - Machine Learning from Disaster** dataset from Kaggle.

- Training dataset: 891 passengers
- Official test dataset: 418 passengers
- Target variable: `Survived`
  - 0 = Not Survived
  - 1 = Survived

The dataset is not included in this repository due to its size and Kaggle competition data requirements.

## ⚙️ Project Workflow

### 1. Data Exploration
- Examining dataset structure and data types.
- Analyzing missing values.
- Exploring survival distribution.
- Generating statistical summaries and visualizations.

### 2. Feature Engineering

Created additional features to improve model performance:

- **Title:** Extracted passenger titles from names.
- **FamilySize:** Calculated family size using SibSp and Parch.
- **IsAlone:** Identified passengers traveling alone.
- **CabinDeck:** Extracted the first letter of the Cabin column.

Removed unnecessary identifier and high-cardinality text columns.

### 3. Data Splitting

Used a stratified 60/20/20 split:

- 60% Training (534 samples)
- 20% Validation (178 samples)
- 20% Holdout Testing (179 samples)

### 4. Data Preprocessing

Implemented preprocessing using Scikit-learn Pipelines and ColumnTransformer.

**Numerical Features:**
- Missing value imputation using Median.
- Feature scaling using StandardScaler.

**Categorical Features:**
- Missing value imputation using Most Frequent.
- One-Hot Encoding.

### 5. Model Training & Hyperparameter Tuning

**Random Forest**
- GridSearchCV
- 5-fold Cross-Validation
- 24 parameter combinations

**Support Vector Machine (SVM)**
- GridSearchCV
- 5-fold Cross-Validation
- 12 parameter combinations

### 6. Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

## 📈 Results

### Validation Results

| Metric | Random Forest | SVM |
|---|---:|---:|
| Accuracy | 85% | 80% |
| Precision (Survived) | 86% | 75% |
| Recall (Survived) | 72% | 72% |
| F1-score (Survived) | 78% | 74% |

### Holdout Test Results

| Metric | Random Forest | SVM |
|---|---:|---:|
| Accuracy | 83% | 82% |
| Precision (Survived) | 82% | 78% |
| Recall (Survived) | 71% | 72% |
| F1-score (Survived) | 76% | 75% |

**Final Selected Model: Random Forest**

Random Forest achieved the higher validation F1-score and was selected for generating predictions on the official Kaggle test dataset.

## 📁 Repository Contents

- `notebook584beebc6a-2.ipynb` — Complete project notebook.

## 🛠️ Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Kaggle Notebooks

## 🚀 How to Run

1. Open the notebook using Kaggle or Google Colab.
2. Attach or upload the Titanic dataset.
3. Install the required Python libraries if needed.
4. Run the notebook cells sequentially.
5. Review model evaluation results.
6. Generate predictions for the official Kaggle test dataset.

**Note:** The notebook currently uses Kaggle dataset paths. Update the file paths if running in another environment.
## 📊 Model Performance Comparison

Two machine learning models were implemented and evaluated:

- Random Forest Classifier
- Support Vector Machine (SVM)

### Validation and Holdout Results

| Metric | Random Forest | SVM |
|---|---:|---:|
| Validation Accuracy | 84.83% | 80.34% |
| Validation Precision | 85.96% | 75.38% |
| Validation Recall | 72.06% | 72.06% |
| Validation F1-score | 78.40% | 73.68% |
| Holdout Accuracy | 82.68% | 81.56% |
| Holdout F1-score | 75.97% | 75.19% |

### Conclusion

Random Forest achieved the best overall performance, outperforming SVM in validation accuracy, precision, F1-score, and holdout metrics.

Therefore, Random Forest was selected as the better-performing model for this project.

## 📌 Project Notes

- Hyperparameter tuning was performed using GridSearchCV with 5-fold cross-validation.
- Preprocessing was integrated into pipelines to reduce data leakage during cross-validation.
- The official Kaggle test dataset does not contain survival labels, so local accuracy cannot be calculated for it.
- The final predictions are saved as `submission.csv`.
- Model comparison results are saved as `model_comparison.csv`.

## 👩‍💻 Author

**Jana Medhat**

Artificial Intelligence Student

[GitHub Profile](https://github.com/medhatj17-svg)

---

⭐ If you find this project interesting, feel free to explore the notebook!
