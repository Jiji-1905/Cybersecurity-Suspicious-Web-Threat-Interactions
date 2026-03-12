# 🔐 Cybersecurity: Suspicious Web Threat Interactions

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-yellow)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-red)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data%20Visualization-blueviolet)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-lightblue)

![Data Analysis](https://img.shields.io/badge/Data%20Analysis-Project-success)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Anomaly%20Detection-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Cybersecurity-critical)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# 📌 Project Overview

**Cybersecurity: Suspicious Web Threat Interactions** is a **Data Analysis and Machine Learning project** that analyzes web traffic logs to identify **potential cyber threats and suspicious activities**.

The project uses **AWS CloudWatch traffic data** to detect anomalies in web interactions and understand patterns in malicious traffic.

This project demonstrates **data analysis, feature engineering, visualization, and anomaly detection using machine learning models.**

---

# 🎯 Project Objectives

* Analyze **web traffic patterns**
* Detect **anomalous interactions**
* Identify **suspicious network behaviors**
* Understand **attack patterns based on traffic features**
* Build **machine learning models for threat detection**

---

# 🗂 Dataset Information

The dataset contains **web traffic records collected using AWS CloudWatch**.

Each record represents a **network interaction with the web server**.

### Key Features

| Column              | Description                  |
| ------------------- | ---------------------------- |
| bytes_in            | Bytes received by the server |
| bytes_out           | Bytes sent from the server   |
| creation_time       | Connection start time        |
| end_time            | Connection end time          |
| src_ip              | Source IP address            |
| src_ip_country_code | Country of the source IP     |
| protocol            | Communication protocol       |
| response.code       | HTTP response code           |
| dst_port            | Destination server port      |
| dst_ip              | Destination IP address       |
| detection_types     | Type of security detection   |

Dataset Size:

* **282 records**
* **16 columns**

---

# 🛠 Tools & Technologies

| Category              | Tools                      |
| --------------------- | -------------------------- |
| Programming           | Python                     |
| Data Analysis         | Pandas, NumPy              |
| Visualization         | Matplotlib, Seaborn        |
| Machine Learning      | Scikit-Learn               |
| Deep Learning         | TensorFlow / Keras         |
| Network Visualization | NetworkX                   |
| Development           | Jupyter Notebook / VS Code |

---

# ⚙️ Project Workflow

## 1️⃣ Data Import

* Load dataset
* Inspect structure
* Check missing values

```python
data.info()
data.head()
```

---

# 🧹 Data Preprocessing

Steps performed:

* Handling missing values
* Removing incomplete records
* Converting timestamps to datetime format

```python
data['creation_time'] = pd.to_datetime(data['creation_time'])
data['end_time'] = pd.to_datetime(data['end_time'])
```

---

# 🔧 Feature Engineering

New features were created to improve analysis:

### Session Duration

```
session_duration = end_time - creation_time
```

### Average Packet Size

```
avg_packet_size = (bytes_in + bytes_out) / session_duration
```

These features help detect **abnormal traffic behaviors.**

---

# 📊 Exploratory Data Analysis

Key visualizations created:

### Traffic Distribution

* Bytes In vs Bytes Out

### Protocol Usage

* Distribution of communication protocols

### Country Based Interactions

* Traffic frequency by source country

### Suspicious Activity by Port

* Detection of unusual destination ports

---

# 🤖 Machine Learning Models

## 1️⃣ Anomaly Detection

**Isolation Forest Algorithm**

Purpose:
Detect unusual traffic patterns automatically.

Features used:

* bytes_in
* bytes_out
* session_duration
* avg_packet_size

Output:

* Normal traffic
* Suspicious traffic

---

## 2️⃣ Random Forest Classifier

Used for **binary classification** of suspicious traffic.

Results:

```
Accuracy: 100%
```

---

## 3️⃣ Deep Learning Model

Neural Network built using **TensorFlow/Keras**

Architecture:

* Dense layers
* Dropout layers
* Sigmoid output layer

Result:

```
Test Accuracy: 100%
```

---

# 📈 Key Insights

Some interesting findings from the analysis:

✔ High **bytes_in with low bytes_out** may indicate infiltration attempts
✔ Repeated traffic from certain **country codes** suggests bot activity
✔ Suspicious interactions frequently occur on **specific ports**
✔ Machine learning models effectively detect anomalous patterns

---

# 📊 Visualization Examples

* Traffic distribution plots
* Country interaction charts
* Anomaly detection scatter plots
* Network interaction graphs (Source IP → Destination IP)

---

# 📁 Project Structure

```
Cybersecurity-Suspicious-Web-Threat-Interactions
│
├── csv_files
│   └── CloudWatch_Traffic_Web_Attack.csv
│
├── outputs
│   ├── Traffic_Distribution.png
│   ├── Protocol_Count.png
│   ├── Country_Interactions.png
│   └── Anomaly_Detection.png
│
├── notebooks
│   └── Cybersecurity_Analysis.ipynb
│
└── README.md
```

---

# 🚀 How to Run the Project

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Jiji-1905/cybersecurity-web-threat-analysis.git
```

### 2️⃣ Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow networkx
```

### 3️⃣ Run Notebook

[Open in **Jupyter Notebook or VS Code** and execute all cells.
](https://colab.research.google.com/drive/1npgDCcIdG0UVsDmR-4HuskQOub67XNAm?usp=sharing)
---

# 📌 Future Improvements

Possible enhancements:

* Real-time threat detection
* Integration with SIEM tools
* Deployment using Streamlit dashboard
* More advanced anomaly detection models
* Larger cybersecurity datasets

---

# 👨‍💻 Author

**Jiji Babu**
**Data Analyst**

Skills:

* Data Analysis
* Python
* Machine Learning
* Data Visualization
* SQL

---

