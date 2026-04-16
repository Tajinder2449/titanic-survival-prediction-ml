# 🚢 Titanic Survival Prediction (Logistic Regression)

## 📌 Project Overview

This project is part of the **"Data Science With Python: From Data to Machine Learning in 5 Days"** bootcamp organized by DevTown.

The goal of this project is to analyze the Titanic dataset and build a machine learning model to predict whether a passenger survived or not using **Logistic Regression**.

---

## 🎯 Objective

* Apply a complete **data science workflow**
* Perform **data cleaning & preprocessing**
* Conduct **exploratory data analysis (EDA)**
* Build a **predictive model**
* Evaluate model performance using standard metrics

---

## 📊 Dataset Information

* **Dataset Name:** Titanic-Dataset.csv
* **Total Records:** 891 passengers
* **Total Features:** 12 columns
* **Target Variable:** `Survived` (0 = No, 1 = Yes)
* **Source:** Kaggle

---

## 🛠️ Tools & Technologies

* **Python**
* **NumPy** – numerical operations
* **Pandas** – data manipulation
* **Matplotlib** – basic visualization
* **Seaborn** – advanced visualization
* **Scikit-learn** – machine learning
* **Google Colab** – development environment

---

## 🔄 Project Workflow

1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Data Visualization
5. Feature Engineering & Encoding
6. Model Building & Evaluation

---

## 🧹 Data Cleaning & Preprocessing

### Missing Values Handling

* **Age:** Filled with mean (~29.7)
* **Cabin:** Dropped (too many missing values)
* **Embarked:** Filled with most frequent value ('S')

### Columns Removed

* PassengerId
* Name
* Ticket
* Cabin

### Feature Engineering

Created a new feature:

```python
df['Family Size'] = df['SibSp'] + df['Parch']
```

---

## 🔢 Categorical Encoding

* **Sex:** male = 0, female = 1
* **Embarked:** S = 0, C = 1, Q = 2

---

## 📈 Exploratory Data Analysis

### Key Insights

* Female survival rate: **93.68%**
* Male survival rate: **42.06%**
* Higher class passengers paid higher fares and had better survival chances
* Most passengers traveled in small families or alone

---

## 🤖 Machine Learning Model

### Algorithm Used

**Logistic Regression**

* Suitable for binary classification
* Simple and interpretable
* Good baseline model

### Train-Test Split

* Training: 80%
* Testing: 20%
* `random_state = 42`

### Model Configuration

```python
model = LogisticRegression(max_iter=1000)
```

---

## 📊 Model Performance

### Accuracy

* **Test Accuracy:** 82.93%

### Confusion Matrix

|          | Predicted 0 | Predicted 1 |
| -------- | ----------- | ----------- |
| Actual 0 | 5           | 3           |
| Actual 1 | 4           | 29          |

### Interpretation

* Strong performance in predicting survivors
* Balanced handling of both classes
* Few false predictions

---

## 🔍 Key Findings

* Gender is the **strongest predictor** of survival
* Passenger class significantly impacts survival probability
* Younger passengers had higher survival chances
* Fare correlates with class and survival

---

## ✅ Conclusion

This project demonstrates a complete data science pipeline from raw data to predictive modeling.

The Logistic Regression model achieved **82.93% accuracy**, showing that even simple models can perform well with proper data preprocessing.

---
📄 [**PDF Version:**](https://tajinder2449.github.io/titanic-survival-prediction-ml/Titanic-Colab.pdf) 
A PDF export of the Jupyter Notebook is included for easy viewing without needing to run the code.

---

## 📁 Project Files

* `Titanic-Dataset.csv` – Raw dataset
* `Cleaned Dataset.csv` – Processed dataset
* `Titanic-Colab.ipynb` – Full code notebook
* `README.md` – Project documentation

---

## 🎓 Bootcamp Submission

This project was created as part of:

**Data Science With Python: From Data to Machine Learning in 5 Days**
Organized by **DevTown (YouTube live Bootcamp)**

---

## ⭐ Acknowledgements

* Kaggle for the dataset
* DevTown for the bootcamp
