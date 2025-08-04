# ml-cyberattack-detector
A hybrid cybersecurity attack detection system that combines rule-based filtering with a machine learning (Random Forest) model to accurately detect network intrusions. Built using the UNSW-NB15 dataset, this project demonstrates layered threat detection, feature importance analysis, and real-time classification strategies.
# 🛡️ The Art and Science of Cybersecurity Attack Detection: A Hybrid Approach

This project explores a **hybrid approach to cybersecurity attack detection**, combining **rule-based systems** with **machine learning models** to analyze and identify potential cyber threats in network traffic data.

## 📌 Overview

With the rise of cyber threats, traditional signature-based detection methods often fall short. This project implements a **two-layer detection system** using:

1. 🧠 Rule-Based Systems – for explainable and fast initial filtering.
2. 🤖 Machine Learning (Random Forest) – for deeper, complex anomaly detection.

The project uses the **UNSW-NB15 dataset**, developed by the University of New South Wales, containing over 250,000 network traffic samples with 9 types of attacks.

---

## 🎯 Objectives

- Understand the key indicators of cyber attacks.
- Build a detection pipeline combining rules and ML.
- Evaluate models using metrics like recall, accuracy, and precision.
- Analyze feature importance for human interpretability.
- Discuss the role of network variables in attack detection.
- Explore security implications in cloud services.

---

## 🧰 Tools & Libraries Used

- Python (Pandas, NumPy, Matplotlib, Seaborn, scikit-learn)
- `dtreeviz` for decision tree visualization
- JupyterLab (via IBM Skills Network Labs)
- Dataset: [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

---

## 📂 Dataset Info

- Combined training & testing: ~257,000 records
- 43 features + 2 target variables (`label`, `attack_cat`)
- 9 types of attacks detected:
  - Fuzzers, DoS, Exploits, Worms, Reconnaissance, Shellcode, Generic, Backdoor, Analysis

---

## ⚙️ Approach

### 1. Rule-Based Detection
- Rules were crafted based on feature thresholds (e.g., `sttl`, `sinpkt`, `synack`).
- Decision tree used to derive explainable logic.
- Achieved **100% recall** for initial filtering.
- Filtered out ~23% of benign traffic before applying ML.

### 2. Machine Learning Model
- **Random Forest Classifier**
- Trained on the filtered dataset
- Performance:
  - **Recall:** 95.7%
  - **Precision:** 96.4%
  - **Accuracy:** 93.5%

### 3. Feature Analysis
- Most important features for attack detection:
  - `sttl`, `ct_state_ttl`, `rate`, `dload`, `sload`, `ct_dst_src_ltm`
- Correlation and importance ranking aligned well.

---

## 📊 Visualization Highlights

- Heatmaps of feature correlations
- Decision tree visualization (`dtreeviz`)
- Confusion matrix of predictions
- Feature importance bar chart

---

## ☁️ Cloud Security Discussion

Discussed challenges in securing cloud infrastructure:
- Shared responsibility
- Multi-tenancy
- Data privacy and compliance (e.g., GDPR, HIPAA)
- DDoS and malware threats

---

## 🤔 Why This Matters

Combining explainable rules with powerful ML detection creates a more **robust**, **interpretable**, and **effective** security monitoring system. This approach balances **speed, accuracy**, and **human interpretability** – crucial for real-world cybersecurity applications.

---

## 📝 Future Enhancements

- Integrate with tools like **Snort** for real-time network intrusion detection.
- Extend to cloud-specific datasets and logs.
- Use SHAP for better explainability of ML models.
- Apply deep learning models for further performance gains.

---


