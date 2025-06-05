# 🛠️ Hybrid Predictive Maintenance using Enhanced CMAPSS NASA Dataset

> 🔍 A multi-phase machine learning solution to predict, classify, and interpret progressive equipment degradation  
> 🚁 Real-world application: Turbofan Jet Engine Failure Prediction  
> 👨‍🔧 From clustering raw sensor data to computing actionable risk scores

---

## 📌 Problem Statement

Traditional predictive maintenance often only predicts **whether a failure will occur**, not **how, when, or how bad**. This project addresses that gap by:

- Introducing **multi-stage degradation labeling** (Normal → Slightly Degraded → Moderately Degraded → Critical → Failure)
- Predicting **remaining useful life (RUL)** per stage
- Computing a **Risk Score** to optimize maintenance schedules and avoid critical failures

---

## 📂 Dataset

- **Source**: [CMAPSS NASA Jet Engine Dataset](https://www.kaggle.com/datasets/behrad3d/nasa-cmaps)
- **Sensor Data**: Multi-dimensional time-series data from aircraft engines (temperature, pressure, vibration, etc.)
- **Custom Labels**: Derived using unsupervised clustering instead of traditional binary or RUL labels

---

## 🚀 Innovation Highlights

### ✅ Multi-Stage Degradation System  
- Clustering used to define degradation levels (0–4)  
- PCA/t-SNE visualizations validate degradation paths

### ✅ Dual-Model Architecture  
- **Classifier**: Predicts degradation stage  
- **Regressor**: Predicts time to next stage  
- Ensemble gives **stage + timeline** insight

### ✅ Real-Time Risk Score  
`Risk Score = Failure Probability × Time Left`  
Used for triggering smart maintenance alerts  
Visualized across engine cycles for operational clarity

---

## 🧠 ML Pipeline

graph TD
A[Raw Sensor Data] --> B[Unsupervised Clustering]

B --> C[Label Multi-Stage Degradation]

C --> D[Classification Model (Stage Prediction)]

C --> E[Regression Model (Time to Next Stage)]

D & E --> F[Risk Score Computation]

F --> G[Maintenance Alerts & Visualization]


---

## 📊 Results Snapshot

| Task                  | Model           | Key Metric            | Value        |
|-----------------------|------------------|------------------------|--------------|
| Stage Classification  | Random Forest    | F1-score (Stage 4)     | 0.93         |
| RUL Regression        | Ridge Regressor  | RMSE                   | 9.4 cycles   |
| Risk Score            | Hybrid Logic     | PR-AUC                 | 0.91         |

---

## 🛠 Tech Stack

- Python, Jupyter Notebook  
- Pandas, NumPy, Seaborn, Matplotlib  
- Scikit-learn, XGBoost, SHAP  
- KMeans, Agglomerative Clustering  
- PCA, t-SNE, SMOTE

---

## 💡 Real-World Value

✔️ **No black-box RUL**: Fully interpretable degradation stage logic  
✔️ **Industry scalability**: Works with any sensor-rich system  
✔️ **Data-driven decision-making**: Helps reduce downtime and optimize cost

---

## 📈 Visualizations

- 📌 Degradation stage evolution  
- 🔍 Confusion matrices per stage  
- 📉 Risk Score trends over engine cycles  
- 💡 SHAP-based feature contribution

---

## 🔮 Future Scope

- Deploy real-time risk dashboards with **Streamlit**  
- Use **LSTM** for sequence modeling  
- Integrate with IoT platforms (e.g., AWS IoT, Azure Digital Twins)

---

## 📬 Contact

**Author**: V Shashank  
**LinkedIn**: [linkedin.com/in/vanga-shashank-925426315](https://linkedin.com/in/vanga-shashank-925426315)  
**Email**: vangashashank1@gmail.com


---

> ✨ This project reflects my ability to build smart, explainable AI for industrial reliability.  
Feel free to connect for discussions, internships, or full-time roles!


