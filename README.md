
# 🚀 Asteroid Hazard Prediction using Machine Learning

This project uses various machine learning classifiers to predict whether an asteroid is hazardous, based on NASA's close-approach data. It includes preprocessing, visualization, and comparison of multiple classification algorithms.

---

## 📁 Dataset

- **Source**: NASA’s Near Earth Object (NEO) dataset.
- **Format**: CSV file
- **Key Features**:
  - Relative Velocity
  - Miss Distance
  - Estimated Diameter
  - Orbit ID, Equinox, etc.

---

## 🧹 Data Preprocessing

- Dropped irrelevant columns (`Name`, `Orbit ID`, etc.)
- Converted `Hazardous` column into binary labels using one-hot encoding.
- Removed features with high correlation and redundancy (e.g., distances in multiple units).
- Categorical columns like `Orbiting Body` and `Equinox` were dropped due to low uniqueness or relevance.

---

## 📊 Visualizations

- Heatmaps of feature correlations before and after dimensionality reduction.
- Bar plot of feature importance using Random Forest.

---

## 🧠 Models Used

### 1. Random Forest Classifier
- Fit on training data with 100 trees.
- Feature importance was visualized using Seaborn.

### 2. Naive Bayes (GaussianNB)
- Simple and fast model.
- Permutation importance used for interpretability.

### 3. Support Vector Machine
- Linear kernel used.
- Effective on high-dimensional data.

### 4. Logistic Regression
- Basic linear model for binary classification.

### 5. K-Nearest Neighbors (KNN)
- Used `k=7` for prediction.
- Distance-based classifier.

### 6. XGBoost
- Gradient boosting with regularization.
- One of the best-performing models in this project.

### 7. AdaBoost
- Adaptive boosting ensemble model.
- Trained with 50 estimators and a learning rate of 1.

---

## 📈 Evaluation

- Used `accuracy_score` and `classification_report` for each model.
- Metrics included Precision, Recall, and F1-Score.

---

## ✅ Results

All models were compared on the test set to find the most effective method for predicting hazardous asteroids. XGBoost and Random Forest yielded the best performance.

---

## 🧾 Conclusion

This project showcases a full machine learning pipeline—from data cleaning to model evaluation—for a real-world problem using public space science data.

---

## 📌 Dependencies

- pandas, numpy
- seaborn, matplotlib
- scikit-learn
- xgboost
