# Titanic Survival Prediction

This project is a beginner-friendly **Machine Learning pipeline** using the classic [Titanic dataset from Kaggle](https://www.kaggle.com/c/titanic).  
The goal is to **predict which passengers survived the Titanic shipwreck** based on their personal and travel attributes.

---

## **Project Overview**

The pipeline includes:

1. **Data Loading and Exploration**
   - Load train and test datasets using `pandas`.
   - Explore missing values, feature distributions, and basic statistics.

2. **Data Preprocessing**
   - Handle missing values (`Age`, `Fare`, `Embarked`).
   - Convert categorical variables to numeric (`Sex`, `Embarked`, `Title`).
   - Feature engineering:
     - `Title` extracted from `Name` (e.g., Mr, Mrs, Miss)
     - `FamilySize` = `SibSp + Parch + 1`
     - `IsAlone` = 1 if passenger traveled alone, 0 otherwise
   - Drop irrelevant columns: `Name`, `Ticket`, `Cabin`.

3. **Modeling**
   - Train a **Random Forest Classifier**.
   - Evaluate model using a validation split (optional if doing cross-validation).

4. **Prediction**
   - Apply trained model to the test dataset.
   - Generate a CSV file suitable for Kaggle submission.

---

## **Getting Started**

### **Requirements**
- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

Install dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
