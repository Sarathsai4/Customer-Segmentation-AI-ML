#  AI-Powered Customer Segmentation with RFM + KMeans + Streamlit

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

##  Project Overview

> This project implements an advanced customer segmentation pipeline by combining **RFM feature engineering**, **K-Means clustering**, and an AI-based classifier for segment prediction. A **Streamlit web app** supports real-time customer lookup and marketing insights—designed to power strategic GTM decisions for companies like YouTube, Amazon, or eCommerce platforms.

---

##  Tech Stack
| Skill / Tool                                                                                                                                                                                                                  | Purpose                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="30" /> **Python**                                                                                                             | Core programming language                     |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="30"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="30" /> **Pandas / NumPy** | Data wrangling and feature creation           |
| <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" width="30" /> **scikit-learn**                                                                                                     | KMeans, Random Forest, preprocessing          |
| <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/streamlit/streamlit-original.svg" width="30" /> **Streamlit**                                                                                                    | Interactive dashboard deployment              |
| 🧮 **PCA / Z-Score**                                                                                                                                                                                                          | Dimensionality reduction and outlier handling |
| <img src="https://matplotlib.org/_static/images/logo2.svg" width="30"/> <img src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" width="60"/> **Matplotlib / Seaborn**                                             | Plotting and EDA                              |
                            

---

## 📂 Folder Structure
```
customer-segmentation-ai/
├── data/ # Raw input transaction data
├── models/ # Saved KMeans and RF model
├── app/ # Streamlit app
├── outputs/ # Cluster visuals and PCA plots
├── Customer_Segmentation.ipynb
└── README.md

```

---

## 🔍 Key Features

| Step | Description |
|------|-------------|
| 📦 Data Loading            | 200K+ transactions across customer IDs, invoices, and sales |
| 📊 RFM Feature Engineering | Derived Recency, Frequency, and Monetary values |
| 🧹 Preprocessing           | Z-score filtering and standardization using `StandardScaler` |
| 🔀 Clustering              | Optimal k found via Elbow Method; segmented with `KMeans(n_clusters=4)` |
| 📉 Dimensionality Reduction| PCA-based 2D visualization for intuitive segment plots |
| 🧠 AI Segment Prediction   | `RandomForestClassifier` trained to predict segment from RFM |
| 💻 Web App Integration     | Built a Streamlit app to view, query, and simulate segmentation |
| 🧭 Strategic Mapping       | Action plans tied to each customer segment (retargeting, upselling, reactivation)

---

## 🤖 Streamlit App Preview

A user-facing Streamlit app supports:

- 🔍 Entering customer RFM values to view predicted segment
- 📈 Exploring segment behaviors interactively
- 🧩 Suggestions for targeting strategies per segment

---

## 📈 Segment Descriptions

| Segment Name         | Traits                                      | Suggested Action                         |
|----------------------|---------------------------------------------|------------------------------------------|
| High-Value Loyalists | Recent, frequent, high-spenders             | Prioritize VIP service, offer exclusives |
| At-Risk Customers    | Long since last purchase, low spend         | Send urgent reactivation incentives      |
| Occasional Buyers    | Moderate activity and revenue               | Target with bundles or subscriptions     |
| New Users            | Just onboarded, low value/frequency         | Nurture with onboarding campaigns        |

---

## 📊 Model Performance

- **Model**: `RandomForestClassifier`
- **Test Accuracy**: `91%`
- **Feature Importance**: `Monetary > Frequency > Recency`
- **Scalability**: Extendable for real-time GTM use cases

---

## 🚀 Future Roadmap
- [ ] Integrate SHAP-based model explainability
- [ ] Add product-category-level segmentation
- [ ] Include session duration & page views in features

---

## ▶️ How to Run

```bash
# Step 1: Install dependencies
pip install -r requirements.txt

# Step 2: Launch Notebook
jupyter notebook Customer_Segmentation.ipynb

# Step 3: Run Web App
cd app
streamlit run app.py
