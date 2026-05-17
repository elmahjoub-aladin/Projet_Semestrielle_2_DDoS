# DDoS Attack Detection Using Machine Learning

A machine learning-based intrusion detection system for identifying Distributed Denial of Service (DDoS) attacks in network traffic using the CICIDS2017 dataset.

---

## Project Overview

This project presents an end-to-end cybersecurity pipeline for detecting DDoS attacks using supervised machine learning techniques.

The system includes:

- Data preprocessing and cleaning
- Feature engineering
- Class balancing using SMOTE
- Machine learning model training
- Model evaluation
- Explainable AI (SHAP & LIME)
- Visualization and performance analysis

The project was developed using Python and Scikit-learn.

---

## Dataset

The project uses the **CICIDS2017** dataset provided by the Canadian Institute for Cybersecurity.

### Dataset File

- `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`

### Dataset Features

The dataset contains:
- Network flow statistics
- Packet-based features
- Byte-based features
- Timing information
- Traffic labels:
  - `BENIGN`
  - `DDoS`

---

## Technologies Used

### Programming Language
- Python 3

### Libraries
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- SHAP
- LIME

---

## Machine Learning Models

The following models were evaluated:

- Random Forest
- Support Vector Machine (SVM)

Random Forest achieved the best overall performance.

---

## Project Pipeline

### 1. Data Loading
- Import CICIDS2017 CSV file

### 2. Data Cleaning
- Remove duplicates
- Handle missing values
- Remove infinite values
- Outlier detection

### 3. Feature Engineering
Creation of additional features such as:
- Packet rate
- Traffic ratio
- Statistical flow metrics

### 4. Data Balancing
- SMOTE oversampling applied on training data

### 5. Data Scaling
- RobustScaler normalization

### 6. Model Training
- Train supervised ML classifiers

### 7. Evaluation
Metrics used:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### 8. Explainability
- SHAP global/local explanations
- LIME explanations
- Feature importance analysis

---

## Results

| Model | Accuracy | ROC-AUC |
|------|------|------|
| Random Forest | 99.1% | 0.997 |
| SVM | 97.9% | 0.993 |

---

## Explainable AI

The project integrates Explainable AI techniques to improve transparency and interpretability.

### SHAP
Used for:
- Global feature importance
- Local prediction explanations

### LIME
Used for:
- Individual prediction explanations

---

## Project Structure

```bash
project/
│
├── data/
│   └── CICIDS2017.csv
│
├── notebooks/
│   └── DDOS(Alaa_&_Amjed).ipynb
│
├── images/
│   ├── confusion_matrix.png
│   ├── shap_summary.png
│   └── lime_explanation.png
│
├── README.md
│
└── requirements.txt
