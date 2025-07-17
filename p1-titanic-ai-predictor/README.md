# 🛳️ Project 1: Titanic Survival Prediction

This project builds a machine learning model to predict survival outcomes of Titanic passengers using data preprocessing, feature engineering, and a Random Forest Classifier. The dataset comes from the popular Titanic Kaggle challenge.

---

## 📊 <u>Dataset:</u>

| Attribute | Details |
|-----------|---------|
| Source | https://www.kaggle.com/competitions/titanic|
| Target | Survived (0 = No, 1 = Yes) |
| Features | Pclass, Sex, Age, SibSp, Parch, Fare, Embarked |

---

## ⚙️ <u>Pipeline Overview:</u>

1. Preprocessing Steps:
   * Dropped: PassengerId, Name, Ticket, Cabin
   * Numerical Features: Age, Fare
     * Imputed using median
     * Scaled using StandardScaler 
   * Categorical Features: Pclass, Sex, SibSp, Parch, Embarked 
     * Imputed using most frequent value 
     * One-hot encoded
2. Model Pipeline 
   * Combined using ColumnTransformer and Pipeline 
   * Classifier: RandomForestClassifier(random_state=42)

---

## 🧠 <u>Model Training & Evaluation:</u>

| Step               | Description |
|--------------------|-------------|
| Split Ratio        | 80% Train / 20% Test |
| Evaluation Metrics | Accuracy, Precision, Recall, F1 |
| Model Used         | Random Forest Classifier |

#### <u>Example Output:</u>

| Parameter | Value |
|-----------|-------|
| Accuracy | 0.8212290502793296 |
| Precision | 0.8 |
| Recall | 0.7567567567567568 |
| F1 Score | 0.7777777777777778 |

#### <u>Classification Report:</u>
````
               precision    recall  f1-score   support

           0       0.83      0.87      0.85       105
           1       0.80      0.76      0.78        74

    accuracy                           0.82       179
   macro avg       0.82      0.81      0.81       179
weighted avg       0.82      0.82      0.82       179
````

#### <u>Confusion Matrix:</u>
````
 [[91 14]
 [18 56]]
````

---

## ✅ <u>Features:</u>
- End-to-end preprocessing pipeline
- Handles missing values and categorical variables
- Easily extendable to other models
- Clean and modular code

---