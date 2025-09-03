# 💳 Credit Card Fraud Detection System

A machine learning project to detect fraudulent credit card transactions using the **Credit Card Fraud Detection dataset** (284,807 records, with only 0.17% fraud cases).  

The project demonstrates **handling extreme class imbalance** using SMOTE and training a **Random Forest classifier** optimized for high recall to maximize fraud detection.  

---

## 📂 Dataset
The dataset is publicly available on Kaggle:  
👉 [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

> ⚠️ Note: The dataset is large (~150 MB) and is **not included in this repository**.  
> Please download `creditcard.csv` from Kaggle and place it in the project root folder.

---

## ⚙️ Tech Stack
- **Python 3.9+**
- **Scikit-learn** – ML algorithms & evaluation
- **Imbalanced-learn** – SMOTE for oversampling
- **Pandas, NumPy** – Data handling
- **Matplotlib, Seaborn** – Visualization
- **Jupyter Notebook** – Development

---

## 🧠 Approach
1. **Data Preprocessing**  
   - Train-test split (80/20) with stratification  
   - Applied **SMOTE** to oversample minority class (fraud cases)  

2. **Model Training**  
   - Random Forest with class weights balanced  
   - Tuned for recall to prioritize catching fraudulent transactions  

3. **Evaluation Metrics**  
   - **Recall:** 0.92  
   - **Precision:** 0.85  
   - **F1-Score:** ~0.88  

---

## 📊 Results & Visualizations

### 🔹 Class Distribution (Before Resampling)
![Class Distribution](./screenshots/class_distribution.png)

### 🔹 Confusion Matrix
![Confusion Matrix](./screenshots/confusion_matrix.png)

### 🔹 Feature Importance
![Feature Importance](./screenshots/feature_importance.png)

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/KomaliG7/credit-card-fraud-detection-System.git
   cd credit-card-fraud-detection-System
````

2. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\\Scripts\\activate    # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and place `creditcard.csv` in the project folder.

5. Run the notebook:

   ```bash
   jupyter notebook fraud_detection.ipynb
   ```

---

## 📌 Project Structure

```
credit-card-fraud-detection/
│── fraud_detection.ipynb    # Main Jupyter Notebook
│── requirements.txt         # Dependencies
│── README.md                # Project Overview
│── screenshots/             # Plots for README
│   ├── class_distribution.png
│   ├── confusion_matrix.png
│   ├── feature_importance.png
│── .gitignore               # Ignore dataset & cache files
```

---

## 📈 Key Takeaways

* Successfully detected **92% of fraudulent transactions** with high recall.
* Balanced fraud detection and false positives (Precision = 0.85).
* Identified key fraud indicators through feature importance analysis.

---

