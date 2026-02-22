# 🛡️ SentinelLogs
## AI-Based Log Anomaly Detection for System Log Security Monitoring

---

## 📌 Project Description
**SentinelLogs** is an AI-powered anomaly detection system designed to identify abnormal patterns in system and authentication logs without relying on known attack signatures.  
The project focuses on behavioral analysis of logs (HDFS dataset) to detect suspicious activities, rare events, and potential security risks from a cybersecurity perspective.

Unlike traditional signature-based detection systems, SentinelLogs learns what is considered **normal behavior** and flags deviations that may indicate misconfigurations, insider threats, or anomalous system activity.

---

## 🎯 Project Objectives
- Define normal behavior in system logs
- Detect anomalies using unsupervised machine learning
- Analyze anomalies from a cybersecurity perspective
- Evaluate false positives and log noise impact
- Simulate real-world SOC (Security Operations Center) usage
- Provide an interpretable anomaly detection pipeline

---

## 🧠 Problem Statement
Modern systems generate massive volumes of logs, making manual monitoring impractical.  
Traditional IDS solutions rely on known signatures and fail to detect unknown or zero-day behaviors.

This project addresses:
- Behavioral anomaly detection in logs
- Insider threat detection
- Noise vs real anomaly differentiation
- Cybersecurity interpretation of anomalies

---

## 📂 Dataset
### Primary Dataset: HDFS Log Dataset (LogHub)
- Type: Real system logs
- Nature: Semi-structured logs
- Labels: Normal / Anomaly (partially labeled)

Dataset folders used:
- `HDFS_v1`
- `HDFS_v2`
- `HDFS_v3`
- `HDFS_2k` (for testing & prototyping)

### Log Attributes
- Timestamp
- Block ID / Node
- Event Type
- Log Message
- Sequence patterns

---

## 🏗️ System Architecture
```code
Raw Logs (HDFS)
↓
Log Parsing & Preprocessing
↓
Feature Engineering
↓
Anomaly Detection Models (ML)
↓
Anomaly Scoring & Thresholding
↓
Security Analysis & Interpretation
↓
SOC Alerts / Dashboard (Future Integration)
```

---

## ⚙️ Methodology

### 1. Log Analysis
- Understanding log structure and patterns
- Identifying frequent vs rare events
- Temporal behavior analysis

### 2. Data Preprocessing
- Log parsing and structuring
- Noise reduction
- Feature extraction
- Encoding categorical variables
- Normalization and scaling

### 3. Feature Engineering
Key engineered features include:
- Event frequency
- Temporal windows
- Event sequence patterns
- Occurrence distribution
- Behavioral frequency metrics

These features help model the baseline of normal system behavior.

---

## 🤖 Machine Learning Models
The project uses unsupervised anomaly detection techniques:

### 🔹 Isolation Forest
- Detects anomalies based on isolation principle
- Efficient for high-dimensional log data
- Suitable for rare event detection

### 🔹 One-Class SVM
- Learns boundary of normal behavior
- Identifies deviations from normal patterns
- Useful for semi-labeled environments

### 🔹 Threshold-Based Detection
- Anomaly score thresholding
- Adaptive interpretation of anomaly levels

---

## 📊 Evaluation Approach
Since anomaly detection is unsupervised, evaluation focuses on:
- Anomaly score distribution
- Detection sensitivity
- False positive analysis
- Interpretability of detected anomalies
- Cybersecurity relevance of flagged events

---

## 🔐 Cybersecurity Interpretation
SentinelLogs is designed with a security-first perspective:
- Anomalies are not automatically classified as attacks
- Rare events may represent benign system behavior
- Log noise is considered in analysis
- Context-aware interpretation is emphasized

Security insights include:
- Suspicious behavioral deviations
- Insider activity indicators
- Abnormal system usage patterns
- Operational anomalies vs malicious anomalies

---

## ⚠️ Limitations
- High false positive risk in noisy log environments
- Context dependency of anomaly interpretation
- Unsupervised models lack explicit attack labeling
- Concept drift (evolving system behavior)
- Dataset-specific bias

---

## 🧪 Technologies & Tools
- Python
- Jupyter Notebook
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Log Parsing Techniques
- Machine Learning (Unsupervised)

---

## 📁 Project Structure
```
SentinelLogs/
│
├── notebooks/
│ ├── 01_EDA_Preprocessing.ipynb
│ ├── 02_Feature_Engineering.ipynb
│ ├── 03_Anomaly_Detection.ipynb
│ └── 04_Security_Analysis.ipynb
│
├── models/
│ └── anomaly_model.pkl
│
├── reports/
│ └── final_report.pdf
│
├── architecture/
│ └── system_architecture.png
│
└── README.md
```

---

## 📘 Notebook Workflow
1. Exploratory Data Analysis (EDA)
2. Log Parsing & Cleaning
3. Feature Engineering
4. Model Training (Isolation Forest, One-Class SVM)
5. Anomaly Detection
6. Security Validation & Interpretation

---

## 🛡️ Security Validation (Key Contribution)
The final phase of the project includes:
- Definition of normal behavior baseline
- False positives analysis
- Log noise impact evaluation
- SOC-oriented interpretation of anomalies
- Risk-based classification of detected anomalies

---

## 🚀 Future Improvements
- Real-time log streaming analysis
- Integration with SIEM/IDS systems (e.g., SOC tools)
- Web-based monitoring dashboard
- Deep learning models (Autoencoders, LSTM)
- Real-time alerting system
- Explainable AI for anomaly justification

---

## 📡 Potential Real-World Applications
- Security Operations Centers (SOC)
- Intrusion Detection Systems (IDS)
- Insider threat detection
- Cloud infrastructure monitoring
- Critical system log auditing
- Behavioral cybersecurity analytics

---

## 📜 Academic Context
This project is developed as part of an academic study in:
- Artificial Intelligence
- Cybersecurity Analytics
- Anomaly Detection in System Logs

The focus prioritizes **quality of analysis and cybersecurity interpretation** over raw model performance.