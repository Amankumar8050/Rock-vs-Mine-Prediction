<div align="center">

# 🪨 Rock vs Mine Prediction
### Binary Classification using SONAR Data & Logistic Regression

[![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![NumPy](https://img.shields.io/badge/NumPy-1.24-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)

![Project Banner](images/chart2_pipeline.png)

</div>

---

## 📌 Overview

This project builds a **binary classification model** to determine whether an underwater object detected by sonar is a **Rock** or a **Mine** — a real-world problem relevant to naval defence and underwater robotics.

Using the **UCI SONAR dataset** (208 samples × 60 frequency-band features), a **Logistic Regression** model is trained and evaluated to classify sonar signal returns with solid accuracy.

---

## 📊 Results

<div align="center">

![Accuracy Chart](images/chart1_accuracy.png)

| Metric | Score |
|--------|-------|
| **Training Accuracy** | 83.42% |
| **Test Accuracy** | 76.19% |
| **Algorithm** | Logistic Regression |
| **Train / Test Split** | 90% / 10% (stratified) |

</div>

---

## 🌊 Sonar Signal Analysis

<div align="center">

![Signal Profile](images/chart3_signals.png)

</div>

The chart above shows the **mean sonar energy per frequency band** for Rocks vs Mines. The distinct signal profiles across the 60 bands are what the model learns to differentiate.

---

## 📁 Project Structure

```
Rock-vs-Mine-Prediction/
│
├── 📓 Rock_vs_Mine_Prediction.ipynb   # Main notebook (EDA + Training + Evaluation)
├── 📄 sonar data.csv                  # UCI SONAR dataset (208 × 61)
├── 🖼️ images/                         # Visualisations & charts
│   ├── chart1_accuracy.png
│   ├── chart2_pipeline.png
│   └── chart3_signals.png
└── 📋 README.md
```

---

## 🧠 How It Works

```
SONAR Signal (60 frequency bands)
         │
         ▼
  Data Preprocessing
  (feature/label split, stratified train-test split)
         │
         ▼
  Logistic Regression Model
  (trained on 187 samples)
         │
         ▼
  Prediction → Rock (R) or Mine (M)
```

---

## 🗃️ Dataset

- **Source:** [UCI Machine Learning Repository — Connectionist Bench (Sonar)](https://archive.ics.uci.edu/ml/datasets/connectionist+bench+(sonar,+mines+vs.+rocks))
- **Samples:** 208 (111 Mines, 97 Rocks)
- **Features:** 60 continuous sonar frequency-band energy values (range 0.0 – 1.0)
- **Label:** `M` = Mine, `R` = Rock

---

## ⚙️ Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/Amankumar8050/Rock-vs-Mine-Prediction.git
cd Rock-vs-Mine-Prediction
```

### 2. Install dependencies
```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 3. Run the notebook
```bash
jupyter notebook Rock_vs_Mine_Prediction.ipynb
```

### 4. Quick prediction (from Python)
```python
import numpy as np
from sklearn.linear_model import LogisticRegression

# After training the model...
sample = [0.0307, 0.0523, ..., 0.0055]   # 60 sonar values
arr    = np.asarray(sample).reshape(1, -1)
pred   = model.predict(arr)[0]
print("Rock" if pred == "R" else "Mine")
```

---

## 🚀 Future Improvements

- [ ] Apply `StandardScaler` for feature normalisation
- [ ] Tune regularisation parameter `C` to reduce train-test gap
- [ ] Benchmark against SVM, Random Forest, and XGBoost
- [ ] Add cross-validation (k-fold) for more robust evaluation
- [ ] Deploy as a simple web app using Streamlit

---

## 👨‍💻 Author

**Aman Kumar**
B.Tech CSE (AI & ML) ||
Government Engineering College Khagaria


[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/amankumar913)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Amankumar8050)

---

<div align="center">

⭐ **Star this repo if you found it useful!**

</div>
