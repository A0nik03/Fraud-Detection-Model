
# 🕵️‍♂️ Fraud Detection Model

Detecting fraudulent financial transactions using machine learning techniques.

This project presents a robust pipeline for analyzing, processing, and classifying fraud-related data using a supervised machine learning approach. It aims to uncover suspicious patterns and improve the security of financial systems.

---

## 📂 Repository Contents

```
.
├── Fraud_Detection.ipynb     # Jupyter notebook with EDA, preprocessing, training, and evaluation
├── README.md                 # Project overview and instructions
└── data/
    └── Fraud.csv             # (Not included in repo - download instructions below)
```

---

## 📊 Dataset Information

- **Name:** `Fraud.csv`
- **Size:** ~400MB
- **Description:** An anonymized transactional dataset with labeled fraudulent and non-fraudulent instances.
- **Shape:** Rows = N (actual rows vary), Columns = Features like amount, time, class, etc.
- **Target Column:** `Class` (1 = Fraud, 0 = Legitimate)

> ❗ **Note:** The dataset is **NOT included** in this repo due to GitHub’s 100MB file size limit. Please follow the instructions below to download and use the data.

---

## 📥 Download Dataset

Upload your dataset to from here:
- [Google Drive](https://drive.google.com/drive/folders/11TNTzTc9VmTLkgTp5ClMFkEfCPXAaA_V?usp=sharing)

Then use the following Python script to download it automatically (example for Google Drive):

### ➤ Features

- **`step`**  
  Represents a unit of time, where **1 step = 1 hour**. The dataset spans **744 steps** (i.e., 30 days).

- **`type`**  
  Type of transaction. It can be one of the following:  
  `CASH-IN`, `CASH-OUT`, `DEBIT`, `PAYMENT`, or `TRANSFER`.

- **`amount`**  
  The value of the transaction, measured in local currency.

- **`nameOrig`**  
  The ID of the person or account that **initiated** the transaction.

- **`oldbalanceOrg`**  
  The sender's account balance **before** the transaction took place.

- **`newbalanceOrig`**  
  The sender's account balance **after** the transaction.

- **`nameDest`**  
  The ID of the person or account **receiving** the transaction.

- **`oldbalanceDest`**  
  The recipient’s account balance **before** the transaction.  
  *Note: For recipients whose IDs start with "M" (merchants), this value may be unavailable.*

- **`newbalanceDest`**  
  The recipient’s account balance **after** the transaction.  
  *Again, may be missing for merchants.*

- **`isFraud`**  
  Indicates whether the transaction is **fraudulent (`1`)** or **legitimate (`0`)**. Fraudulent activity often involves unauthorized transfers and cash-outs.

- **`isFlaggedFraud`**  
  Flags transactions that **violate fraud detection rules** — in this dataset, any `TRANSFER` over **200,000** units is flagged as suspicious.
---

## ⚙️ Tools & Technologies

- Python 3.8+
- Jupyter Notebook
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Git + GitHub

---

## 🧠 Machine Learning Workflow

1. **Exploratory Data Analysis (EDA)**  
   - Correlation matrix  
   - Class imbalance visualization  
   - Feature distributions

2. **Preprocessing**  
   - Handling missing data  
   - Feature scaling (e.g., MinMaxScaler)  
   - Encoding categorical variables (if any)

3. **Modeling**  
   - Logistic Regression  
   - Random Forest  
   - Decision Tree  
   - Other classifiers (optionally)

4. **Evaluation Metrics**  
   - Accuracy, Precision, Recall, F1 Score  
   - Confusion Matrix  
   - ROC-AUC Curve

5. **Handling Imbalanced Data (Optional)**  
   - SMOTE / Oversampling  
   - Undersampling  
   - Class weights

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/A0nik03/Fraud-Detection-Model.git
   cd Fraud-Detection-Model
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. (Optional) Download dataset using the script or place it in `data/Fraud.csv`.

4. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

5. Open `Fraud_Detection.ipynb` and run all cells.

---

## 🔍 Sample Visualizations

- ✅ Distribution of legitimate vs fraud transactions  
- 📈 Feature importance chart from Random Forest  
- 🔍 ROC-AUC for model comparison  
- 📊 Confusion matrix heatmaps
---

## 🧑‍💻 Author

**Bhanu Pratap ([@A0nik03](https://github.com/A0nik03))**  
💼 Passionate about AI, fraud detection systems, and full-stack development.  
🛠️ Building secure, intelligent systems to detect anomalies and prevent scams.

---

## 🪪 License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute it.

---

## 🙌 Contributions

Feel free to:
- Submit issues
- Suggest improvements
- Open pull requests

> Please fork the repo and create a feature branch for contributions.

---

## ⭐ Show Some Love

If you found this project helpful, consider giving it a ⭐ on GitHub!

---
