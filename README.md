# 💧 Water Potability Prediction using Machine Learning

Predicting whether water is safe for drinking is an important public health challenge. In this project, I built an end-to-end machine learning pipeline to classify water samples as **potable** or **non-potable** using physicochemical water quality measurements.

The project covers the complete machine learning workflow—from data preprocessing and exploratory data analysis to model building, hyperparameter tuning, and evaluation.

---

# 📌 Project Overview

The objective of this project is to predict the **potability of water** based on nine water quality parameters.

During the project, multiple preprocessing techniques and machine learning models were explored to identify the most suitable approach for this dataset.

The workflow includes:

- Data preprocessing
- Missing value treatment using KNN Imputation
- Exploratory Data Analysis (EDA)
- Correlation Analysis
- Logistic Regression (Baseline Model)
- Random Forest Classification
- Hyperparameter Tuning using GridSearchCV
- Model Evaluation and Comparison

---

# 📊 Dataset

The dataset contains **3,276** water samples with **9 numerical features** describing various physicochemical properties of water.

### Target Variable

| Value | Meaning |
|--------|---------|
| 0 | Not Potable |
| 1 | Potable |

### Features

- pH
- Hardness
- Solids
- Chloramines
- Sulfate
- Conductivity
- Organic Carbon
- Trihalomethanes
- Turbidity

---

# 🧹 Data Preprocessing

The dataset contained missing values in:

| Feature | Missing Values |
|----------|---------------:|
| pH | 491 |
| Sulfate | 781 |
| Trihalomethanes | 162 |

Different imputation techniques were explored.

- Mean Imputation
- Median Imputation
- **KNN Imputation (Selected)**

KNN Imputation was chosen because it preserved the original feature distributions more effectively than mean or median imputation.

---

# 📊 Exploratory Data Analysis

Several visualizations were performed to better understand the dataset.

The analysis included:

- Distribution plots
- Boxplots
- Feature vs Target analysis
- Correlation Heatmap

### Key Findings

- The dataset is moderately imbalanced (61% non-potable, 39% potable).
- Individual features showed significant overlap between potable and non-potable water samples.
- Correlation analysis revealed weak linear relationships among the features.
- No single feature alone was sufficient for classification.

These findings motivated the use of a tree-based ensemble model capable of learning non-linear relationships.

---

# 🤖 Machine Learning Models

## Logistic Regression

Logistic Regression was used as the baseline classifier.

### Performance

| Metric | Score |
|---------|-------:|
| Accuracy | 0.6098 |
| Precision | 0.0000 |
| Recall | 0.0000 |
| F1 Score | 0.0000 |
| ROC-AUC | 0.5482 |

The model predicted only the majority class, demonstrating that the dataset is not linearly separable.

---

## Random Forest

A Random Forest classifier was then trained to capture complex, non-linear interactions among the features.

### Baseline Performance

| Metric | Score |
|---------|-------:|
| Accuracy | 0.6585 |
| Precision | 0.6356 |
| Recall | 0.2930 |
| F1 Score | 0.4011 |
| ROC-AUC | 0.6469 |

---

# ⚙️ Hyperparameter Tuning

The Random Forest model was optimized using **GridSearchCV** with **5-fold cross-validation**.

### Best Parameters

```python
RandomForestClassifier(
    n_estimators=200,
    max_depth=None,
    min_samples_split=2,
    min_samples_leaf=1,
    random_state=42
)
```

### Tuned Model Performance

| Metric | Score |
|---------|-------:|
| Accuracy | **0.6585** |
| Precision | **0.6270** |
| Recall | **0.3086** |
| F1 Score | **0.4136** |
| ROC-AUC | **0.6470** |

Hyperparameter tuning produced a modest improvement in recall and F1-score while maintaining the same overall accuracy.

---

# 📈 Model Comparison

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|--------|---------:|----------:|-------:|---------:|--------:|
| Logistic Regression | 0.6098 | 0.0000 | 0.0000 | 0.0000 | 0.5482 |
| Random Forest | 0.6585 | 0.6356 | 0.2930 | 0.4011 | 0.6469 |
| Tuned Random Forest | **0.6585** | **0.6270** | **0.3086** | **0.4136** | **0.6470** |

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📁 Project Structure

```
water_potability_prediction/
├── data/
│   └── water_potability.csv
│
├── notebooks/
│   └── machine-learning-final-project-submission.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 🎯 Conclusion

This project demonstrates a complete machine learning workflow for solving a binary classification problem.

While Logistic Regression struggled due to the weak linear relationships present in the dataset, Random Forest significantly improved predictive performance by learning non-linear interactions among water quality features. Hyperparameter tuning further improved the model's ability to identify potable water samples.

The final tuned Random Forest model achieved:

- **Accuracy:** 65.85%
- **F1 Score:** 0.4136
- **ROC-AUC:** 0.6470

making it the best-performing model explored in this project.

---

## 👨‍💻 Author

**Shubhram Priyadarshan**

Machine Learning | Data Analytics | Python
