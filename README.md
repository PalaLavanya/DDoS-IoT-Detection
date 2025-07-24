# DDoS-IoT-Detection
A Machine Learning-based project to detect DDoS attacks in IoT networks.

This project focuses on detecting **Distributed Denial of Service (DDoS)** attacks in **IoT (Internet of Things)** environments using machine learning models and advanced feature selection techniques.

---

## 📂 Dataset

- **Name:** CICIoT2023  
- **Source:** Canadian Institute for Cybersecurity  
- **Description:** Contains IoT traffic with benign samples and 34 types of attacks, including DDoS, DoS, Botnet, etc.  
- **Used For:**  
  - Full 34-class classification  
  - 12-class DDoS-specific classification + benign samples  

---

## ⚙️ Preprocessing

- Filtered relevant classes (34 and 12)  
- Encoded categorical data with `pd.get_dummies()`  
- Scaled features using `MinMaxScaler`  
- Filled missing values using column-wise mean

---

## 🧠 Feature Selection Techniques

- **Chi-Square:** Selected top-k features based on statistical scores  
- **RFE (Recursive Feature Elimination):** Used Decision Tree as the estimator  
- **Hybrid (HFSA):** Combined top features from both Chi-Square and RFE

---

## 🤖 Machine Learning Models

| Model            | Description                                           |
|------------------|-------------------------------------------------------|
| Decision Tree    | Interpretable tree-based model                        |
| Random Forest    | Ensemble of decision trees for improved accuracy      |
| K-Nearest Neighbors (KNN) | Instance-based prediction based on neighbors      |
| XGBoost          | High-performance gradient boosting algorithm          |

---

## 📈 Key Results

- Using **XGBoost** with **Chi-Square selected features**, the model achieved a **maximum accuracy of 99.95%** on 12-class DDoS classification.
- Other models like **Decision Tree**, **Random Forest**, and **KNN** showed moderately high accuracy but XGBoost outperformed all.
- Evaluation metrics include **Accuracy**, **Precision**, **Recall**, **F1 Score**, and **Confusion Matrix**.

---


