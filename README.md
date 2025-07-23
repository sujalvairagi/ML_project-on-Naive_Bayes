# ML_project-on-Naive_Bayes
# 🍽️ Predicting Lunch or Dinner with Naive Bayes (Tips Dataset)

## 👋 Introduction

Welcome! This project is a mini-classification task where we aim to **predict whether a customer dined during Lunch or Dinner** based on their bill amount, tip, and group size.

The dataset used is the popular **`tips` dataset** from the Seaborn library — a great choice for learning classification, preprocessing, and visual analysis.

---

## 🔍 Objective

> **Goal:** Given details like total bill, tip amount, and party size — predict whether the meal was during **Lunch** or **Dinner**.

We use a simple but powerful classifier: **Naive Bayes**, and focus on improving its performance through **feature encoding** and **hyperparameter tuning**.

---

## 🛠️ Steps Followed

### 1. **Data Loading and Exploration**
- Loaded the `tips` dataset from Seaborn
- Explored column types, null values, and the target distribution (`Lunch` vs `Dinner`)

### 2. **EDA (Exploratory Data Analysis)**
- Used `countplot` to check balance between Lunch and Dinner samples
- Used `pairplot` with `hue='time'` to visually see how features differ by meal time

### 3. **Preprocessing**
- Encoded the `time` column using **Label Encoding**
- Applied **One-Hot Encoding** to selected categorical features like `sex`, `smoker`, `day`
- Used `ColumnTransformer` to combine numerical and categorical preprocessing cleanly

### 4. **Model Building**
- Chose **Naive Bayes (CategoricalNB)** as our model — ideal for categorical feature spaces

### 5. **Train-Test Split**
- Split the dataset into training and testing sets using `train_test_split()`

### 6. **Model Training and Evaluation (Before Tuning)**
- Trained the Naive Bayes model
- Evaluated using:
  - **Accuracy**
  - **Classification Report**
  - **Confusion Matrix**

### 7. **Hyperparameter Tuning**
- Used **GridSearchCV** to search for the best value of `alpha` (smoothing)
- Tuned model was re-evaluated for accuracy and confusion matrix

---

## 📈 Results Summary

| Stage              | Accuracy | Notes                           |
|-------------------|----------|----------------------------------|
| Before Tuning     | ~ (your value) | Baseline using default alpha       |
| After Grid Search | ~ (your value) | Improved performance with tuned `alpha` |

---

## 📊 Visuals Included

- Pairplot to observe visual separability of Lunch vs Dinner
- Confusion matrices (before and after tuning) to evaluate true vs predicted labels
- Countplot of target distribution to check for class imbalance

---

## 📌 Key Learnings

- One-hot encoding + Naive Bayes = strong combination for categorical data
- `hue` in `pairplot` is powerful for visual classification intuition
- Hyperparameter tuning using `GridSearchCV` boosts performance when done carefully
- Confusion matrix is crucial to go beyond accuracy

---

## 🧠 Future Enhancements

- Try other classifiers: Logistic Regression, SVM, Decision Trees
- Include more features (e.g., day of the week) with proper encoding
- Add cross-validation visualizations (e.g., accuracy vs alpha)
- Save and deploy the model using `joblib` or Flask

---

## 👨‍💻 Tools & Libraries

- Python 🐍
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (LabelEncoder, GridSearchCV, Naive Bayes)

---

## 🙌 Acknowledgments

- **Seaborn** for the beautiful and beginner-friendly dataset
- **scikit-learn** for clean APIs to experiment and learn from

---

## 💬 Want to Learn More?

Reach out or leave feedback — always up for discussing ML ideas or collaborations! 😊
