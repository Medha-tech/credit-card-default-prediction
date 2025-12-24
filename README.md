# Credit Card Default Prediction

## 📌 Project Overview
This project aims to predict whether a customer will default on their credit card payment using machine learning techniques. The focus is on identifying potential defaulters while handling class imbalance effectively and making business-oriented evaluation decisions.

---

## 📂 Project Structure
```
Credit_Card_Default/
├── data/
│   └── UCI_Credit_Card.csv   
├── Credit_Card_Default.ipynb     
├── README.md                     
├── requirements.txt               
└── .gitignore
```                 

---

## 📊 Dataset
- **Source:** UCI Machine Learning Repository  
- **Target Variable:** `default.payment.next.month`  
- The dataset is **imbalanced**, with fewer defaulters than non-defaulters.

---

## ⚙️ Model Overview

### 1️⃣ Logistic Regression
- Used as a **baseline model**
- Requires feature scaling
- Provides **interpretability**
- Performs well in identifying defaulters but struggles with non-linear patterns

### 2️⃣ Random Forest Classifier
- Captures **non-linear relationships**
- Handles feature interactions automatically
- Trained using **class weighting** to address imbalance
- **Probability threshold tuning** was applied to improve recall for defaulters

---

## 🧠 Key Techniques Used
- Removal of non-informative feature (`ID`)
- Feature scaling for Logistic Regression
- Handling class imbalance using `class_weight='balanced'`
- Threshold tuning for Random Forest (`threshold = 0.45`)

---

## 📈 Evaluation Metrics
Recall and ROC-AUC were prioritized because:
- The dataset is imbalanced
- Missing defaulters is more costly than flagging safe customers

---

## 🏆 Results Summary
- Logistic Regression provided a strong and interpretable baseline.
- Random Forest achieved a **defaulter recall of 0.71** after threshold tuning.
- A trade-off between recall and accuracy was consciously accepted to align with credit risk objectives.

---

## 🛠️ Tools & Libraries
- Python
- NumPy, Pandas
- Scikit-learn
- Matplotlib, Seaborn

---

## 🚀 How to Run
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt

3. Run the notebook


