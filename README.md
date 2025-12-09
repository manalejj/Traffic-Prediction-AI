# 🚄 Rail Transit Delay Prediction System (AI Prototype)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Status](https://img.shields.io/badge/Status-Prototype-green?style=for-the-badge)

> **A Machine Learning framework to forecast train delays by leveraging open transit data.**
> *Note: This project serves as a technical proof-of-concept for predictive maintenance and traffic optimization, applicable to national rail networks (e.g., ONCF).*

---

## 📖 Overview

Predicting transit delays is a critical challenge for modern transportation systems. This project explores the use of **Machine Learning (ML)** and **Deep Learning (DL)** to analyze historical trip updates and vehicle positions to predict arrival delays.

By merging **GTFS (General Transit Feed Specification)** data with real-time updates, this system allows operators to:
* 🔍 **Identify delay patterns** in real-time.
* ⚡ **Optimize scheduling** based on predicted congestion.
* 📢 **Improve passenger information** with accurate ETA updates.

*This repository contains case studies based on open data from Canberra, Dublin, and Sydney rail systems.*

---

## 📊 Key Results & Performance

We evaluated multiple algorithms to ensure robustness. Below are the visual results from our simulation environment.

### 1. Prediction Accuracy (Random Forest)
The Random Forest model achieved an **R² Score of ~0.87** with a Mean Absolute Error (MAE) of **< 1 minute**, demonstrating high reliability for real-time applications.

![Random Forest Results](projet_cv\RF_Result.png)
*(Fig 1: Actual vs. Predicted Delays showing close alignment)*

### 2. Feature Importance Analysis (Gradient Boosting)
Using Gradient Boosting, we identified the key drivers of delays. This analysis allows operators to focus on high-impact factors like **Rush Hour** and **Weather Conditions**.

![Feature Importance](GB_Features.png)
*(Fig 2: Relative importance of factors influencing transit delays)*

### 3. Deep Learning Convergence (DNN)
The Deep Neural Network (DNN) demonstrated strong convergence, minimizing the loss function over training epochs to capture complex non-linear traffic patterns.

![DNN Loss Curve](DNN_Curve.png)
*(Fig 3: Training Loss Curve showing model learning progress)*

### 4. System Overview & Data Flow
Visual representation of the data pipeline and processing architecture.

![System Architecture](YOUR_4TH_IMAGE_NAME.png)
*(Fig 4: Architecture Diagram / Data Visualization)*

---

## 🧠 Models & Methodology

We implemented and compared five distinct algorithms to determine the most effective approach for time-series delay prediction:

| Algorithm | File | Description |
| :--- | :--- | :--- |
| **Random Forest (RF)** | `RF.py` | Ensemble learning method for robust predictions (Best Performer). |
| **Gradient Boosting (GB)** | `GB.py` | High-performance boosting model for structured data & feature analysis. |
| **Support Vector Machines** | `SVM-FS.py` | Includes feature selection and parameter tuning. |
| **Deep Neural Networks** | `DNN.py` | Deep learning architecture for complex pattern recognition. |
| **Linear Regression** | `LR.py` | Baseline model for performance comparison. |

---

## 📂 Project Structure

```bash
├── 📂 Data              # Raw datasets (Canberra, etc.)
├── 📂 Large data        # Substantial files (Trip_Update, Vehicle_Update)
├── 📂 merging           # Scripts for data fusion and preprocessing
├── 📂 plot              # Generated graphs (Actual vs Predicted, Error metrics)
├── 📜 SVM-FS.py         # Support Vector Machine Implementation
├── 📜 RF.py             # Random Forest Implementation (Main Model)
├── 📜 GB.py             # Gradient Boosting Implementation
├── 📜 DNN.py            # Deep Neural Network Implementation
└── 📜 README.md         # Project Documentation
