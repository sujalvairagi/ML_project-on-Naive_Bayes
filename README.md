# Predicting Lunch or Dinner using Naive Bayes (Tips Dataset)

## Introduction

This is a small classification project where I tried to predict whether a meal was Lunch or Dinner based on some details like total bill, tip, and size of the group. I used the `tips` dataset from Seaborn, which is quite popular for basic data analysis and machine learning.

The goal was to understand how a Naive Bayes model works, and how to prepare the data properly before training a classifier.

---

## Objective

The main aim of this project is to classify whether a given entry is a Lunch or Dinner meal using features like:
- Total bill
- Tip amount
- Group size
- Some categorical data like gender, smoking status, and day

I used a Naive Bayes classifier because it’s simple and works well with categorical data. Also, it’s good for learning.

---

## Steps I Followed

### 1. Data Loading and Basic Exploration
- Loaded the tips dataset from Seaborn
- Checked the structure and contents using `info()`, `head()` etc.

### 2. Visual Exploration
- Used a countplot to see how many Lunch and Dinner entries are in the dataset
- Used a pairplot with `hue='time'` to see if features like total bill or tip show any separation between Lunch and Dinner

### 3. Preprocessing
- Used Label Encoding for the target (`time`)
- One-Hot Encoded some categorical features like `sex`, `smoker`, and `day`
- Used `ColumnTransformer` to combine encoding with numeric data

### 4. Model Building
- Trained a basic Naive Bayes model (GaussianNB)
- Used train-test split to evaluate on unseen data

### 5. Evaluation (Before Tuning)
- Calculated accuracy and classification report
- Plotted a confusion matrix to see where the model was going wrong

### 6. Hyperparameter Tuning
- Tried different values of `alpha` using `GridSearchCV`
- Used 5-fold cross-validation and accuracy as the scoring metric
- Evaluated the tuned model again

---

## Results

 Model            | Accuracy     | Comments                              |
                  |              |                                       |
 Before Tuning    | (your value) | Initial baseline                      |
 After Tuning     | (your value) | Slight improvement with tuned `alpha` |

From the confusion matrix and classification report, we can say the model improved a bit after tuning. Most of the correct predictions were on Dinner entries, which is understandable since Dinner is more frequent in the dataset.

---

## Visualizations Used

- Pairplot to see separation between classes
- Countplot to check class balance
- Confusion matrix to evaluate prediction results

---

## What I Learned

- Naive Bayes works well when you handle categorical features properly
- Visualizations like pairplot help a lot to understand data before modeling
- Accuracy is okay when classes are not too imbalanced, but confusion matrix shows more details
- Hyperparameter tuning using GridSearchCV is useful, especially when the model is simple


