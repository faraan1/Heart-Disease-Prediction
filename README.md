# 🫀 Heart Disease Prediction using Machine Learning

A machine learning model to predict the risk of heart disease based on patient health data. This project uses the **Heart Disease UCI Dataset** to build a classification model with Logistic Regression, including data cleaning, exploratory data analysis (EDA), model training, and evaluation.

---

## 📌 Project Overview

Heart disease is one of the leading causes of death worldwide. Early detection can significantly improve patient outcomes. In this project, we develop a predictive model that classifies whether a patient is at risk of heart disease based on clinical and demographic features.

We use **Logistic Regression** for interpretability and strong baseline performance, but the pipeline can be extended to Decision Trees, Random Forests, or other classifiers.

---

## 📚 Dataset

- **Rows**: 303 patients
- **Features**: 13 clinical attributes
- **Target**: `num` → converted to binary:  
  - `0` = No heart disease  
  - `1` = Heart disease present

### 🔍 Features Included:
| Feature | Description |
|--------|-------------|
| `age` | Age in years |
| `sex` | Male/Female |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl |
| `restecg` | Resting ECG results |
| `thalch` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of peak exercise ST segment |
| `ca` | Number of major vessels colored by fluoroscopy |
| `thal` | Thalassemia (blood disorder) type |

---

## 🛠️ Technologies Used

- **Python** (Pandas, NumPy)
- **Data Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn
- **Jupyter Notebook** (for development and analysis)

---

## 🔍 Key Steps

1. **Data Cleaning**
   - Handle missing values (e.g., `?`, blank entries)
   - Impute missing data using median/mode
   - Convert target to binary classification

2. **Exploratory Data Analysis (EDA)**
   - Distribution of heart disease by age, gender, chest pain
   - Correlation heatmap
   - Insights into high-risk indicators

3. **Model Training**
   - Logistic Regression classifier
   - Train-test split (80-20)

4. **Model Evaluation**
   - Accuracy, Confusion Matrix, ROC Curve, AUC
   - Feature importance analysis

5. **Key Findings**
   - Top predictors: `ca`, `thal`, `oldpeak`, `cp`, `exang`
   - Asymptomatic chest pain is a major risk factor

---

## 📊 Model Performance

| Metric | Value |
|-------|-------|
| **Accuracy** | 85.2% |
| **AUC (ROC)** | 90% |
| **Precision (Class 1)** | 83% |
| **Recall (Class 1)** | 89% |

✅ Strong discriminative power with high sensitivity (low false negatives).

---

## 🔑 Most Important Features

| Feature | Importance (Coefficient) |
|--------|--------------------------|
| `ca` | Number of major vessels (strong negative) |
| `thal` | Thalassemia defect type |
| `oldpeak` | ST depression |
| `cp` | Chest pain type |
| `thalch` | Max heart rate achieved |

> 💡 **Insight**: Patients with asymptomatic chest pain or abnormal thal scans are at significantly higher risk — often undetected without screening.
