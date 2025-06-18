# 🧬 Breast Cancer Prediction

## 📌 Overview
This machine learning project predicts whether a breast tumor is **benign (B)** or **malignant (M)** using structured diagnostic data. It covers a full ML pipeline including data preprocessing, exploration, feature selection, model evaluation, and deployment.

## 📊 Dataset
- **Sources**:
  - [Kaggle – Breast Cancer Wisconsin (Diagnostic)](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
  - [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)
- **Size**: 569 rows × 32 columns
- **Target Variable**: `diagnosis` (`M` = Malignant, `B` = Benign)
- **Features**: Cell nucleus characteristics, including radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, and fractal dimension.

## 🧪 Project Pipeline

### 1. **Data Exploration**
- Snapshot and summary statistics
- Column grouping: mean, standard error, worst features

### 2. **Data Cleaning**
- Removed ID, unnamed columns, and duplicates
- Checked for missing values

### 3. **Exploratory Data Analysis (EDA)**
- Target distribution (histogram, pie chart)
- Correlation heatmaps (mean, se, worst)
- Boxplots, violin plots, swarm plots, and pairplots by diagnosis

### 4. **Feature Selection**
- Removed highly correlated features (correlation > 0.92)
- Ranked features using Random Forest importance
- Top 10 features selected for optional compact modeling

### 5. **Modeling**
- Split data into Train (70%), Validation (15%), and Test (15%)
- Scaled data using MinMaxScaler (trained only on training set)
- Trained 7 classifiers:
  - Logistic Regression
  - Random Forest
  - K-Nearest Neighbors
  - Decision Tree
  - Gradient Boosting
  - AdaBoost
  - Support Vector Machine (SVM)

### 6. **Model Evaluation & Optimization**
- Compared models using Accuracy and F1 Score
- Tuned hyperparameters via GridSearchCV
- Best models:
  - **Random Forest (tuned)**: F1 Score ≈ 0.99
  - **Logistic Regression** and **SVM** also performed well

### 7. **Deployment & Interpretation**
- Saved best model and scaler with `joblib`
- Loaded model to make predictions on unseen patient samples
- Returned both prediction and probability (Benign, Malignant)

## 🧠 Final Model Insights
| Metric       | Value |
|--------------|-------|
| Accuracy     | ~99%  |
| F1 Score     | ~99%  |
| Best Model   | `RandomForestClassifier` (tuned) |

The classifier is capable of distinguishing between malignant and benign tumors with high precision. Model interpretability was enhanced through EDA and feature importance visualizations.

## 🔧 Technologies Used
- Python (Pandas, NumPy, Scikit-learn)
- Visualization: Matplotlib, Seaborn, Plotly
- Jupyter Notebook
- Joblib (for model deployment)
- Git / GitHub

## 📈 Results
This project demonstrates that structured medical data can be leveraged to build highly accurate cancer prediction tools. The entire pipeline was implemented end-to-end, with emphasis on interpretability, reproducibility, and model evaluation.

## 👏 Author
**Reza Zare**  
Designed and implemented the full machine learning pipeline, including data cleaning, EDA, feature selection, model training, tuning, and deployment.

## 📎 Credits
Dataset sourced from:
- [Kaggle – Breast Cancer Wisconsin (Diagnostic)](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)

For educational and research purposes only. All rights belong to the original contributors.
