
# 💡 AI-Powered Customer Segmentation with RFM + KMeans + Streamlit

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-FF9900)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-Explainer-blueviolet)
![PCA](https://img.shields.io/badge/PCA-Dimensionality-brightgreen)
![License](https://img.shields.io/badge/license-MIT-green)

---

##  Project Overview

> This project implements an **AI-enhanced customer segmentation system** by combining **RFM feature engineering**, **KMeans clustering**, and a **Random Forest classifier** wrapped into an intuitive **Streamlit web application**. Additionally, it includes **SHAP explainability** and **AI-generated strategic guidance** using the GROQ LLM API.


Originally built on a **retail dataset**, this solution is designed to scale across domains—powering strategic segmentation for YouTube BizOps, eCommerce GTM, and enterprise marketing use cases.


---

## 🛠️ Tech Stack & Tools

| Tool / Tech                                                                                                                                                                                                                      | Role                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="30" /> **Python**                                                                                                               | Programming foundation                                               |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="30" /> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="30" /> **Pandas / NumPy** | Data wrangling & RFM derivation                                     |
| <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" width="30"/> **Scikit-Learn**                                                                                                         | `KMeans`, `RandomForest`, scaling, PCA                              |
| 🧮 **PCA** + 🧾 **Z-Score**                                                                                                                                                                                                      | Dimensionality reduction + anomaly filtering                         |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/streamlit/streamlit-original.svg" width="30" /> **Streamlit**                                                                                                      | App interface for real-time simulation                              |
| 🧊 **SHAP**                                                                                                                                                                                                                       | Interpretable ML using feature importance visualization              |
| 🌐 **GROQ LLM (LLaMA 3)**                                                                                                                                                                                                        | AI-generated targeting strategies from customer input                |
| 📦 **Joblib**                                                                                                                                                                                                                    | Model persistence for KMeans and Random Forest                       |
| 📉 **Plotly / Matplotlib**                                                                                                                                                                                                       | Interactive visualizations and summary charts                        |

---

## 📂 Folder Structure

```
customer-segmentation-ai/
├── app/ # Streamlit app
│ └── app.py
├── data/ # Sample RFM files
├── models/ # Saved models (RF & KMeans)
├── outputs/ # Visualizations and exports
├── Customer_Segmentation.ipynb # Model training + SHAP analysis
└── README.md
```


---

## 📈 Key Concepts

### 🔁 RFM Analysis
RFM stands for:

- **Recency** – Time since the customer’s last purchase
- **Frequency** – Total number of purchases made
- **Monetary** – Total amount spent

This segmentation approach identifies high-value and at-risk customers using behavioral data.

---

## 🧪 Workflow Breakdown

### 1. **Data Preparation**
- Clean transactional records (e.g., InvoiceNo, CustomerID, Amount).
- Derive **RFM scores** by aggregating at the customer level.

### 2. **Standardization & PCA**
- Standardize RFM features using `StandardScaler`.
- Reduce to 2D using **PCA** for interactive visualization.

### 3. **Segmentation via KMeans**
- Apply KMeans with optimal `k=4` to form clusters.
- Store cluster labels and visualize segments on PCA plot.

### 4. **Train Random Forest Classifier**
- Use clustered data as target to train RF model.
- Model serves as a lightweight, interpretable classifier for new customers.

### 5. **SHAP Explainability**
- Integrate `SHAP` to compute feature importance across clusters.
- Provide visual feedback on how features impact predictions.

### 6. **Interactive App (Streamlit)**
- Upload CSV/XLSX with RFM data or simulate single customer input.
- Real-time predictions + **GROQ AI** suggestions for marketing strategy.
- Option to download cluster summaries and visual plots.

---

## 🔍 Example Features in Streamlit App

- 📊 Data Preview with clustering columns
- 📌 PCA Cluster Scatter Plot
- 📈 Segment-wise bubble and pie plots
- ⚙️ SHAP bar chart for feature importance
- 🤖 Segment predictor + marketing recommendations via AI

---

## 🧭 Segment Profiles

| Segment Name         | RFM Behavior                            | Strategy                             |
|----------------------|------------------------------------------|--------------------------------------|
| 🎯 **High-Value Loyalists** | High F & M, low R (frequent recent spenders) | Offer VIP deals, early access        |
| ⚠️ **At-Risk Customers**    | High R, low F & M                      | Winback emails, discount triggers    |
| 🧍 **Occasional Buyers**    | Moderate F and M                      | Promote bundles/subscriptions        |
| 🆕 **New Users**            | Recent entry, low F & M               | Send onboarding & engagement offers  |

---

## 📈 Model Performance

| Metric          | Value            |
|------------------|------------------|
| **Model**        | `RandomForestClassifier` |
| **Test Accuracy**| 91%               |
| **Top Features** | Monetary > Frequency > Recency |

---

## 🧪 How to Run

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Train model (optional)
jupyter notebook Customer_Segmentation.ipynb

# 3. Launch Streamlit app
cd app
streamlit run app.py

