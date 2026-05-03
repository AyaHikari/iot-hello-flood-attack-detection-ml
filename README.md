# IoT Hello Flood Attack Detection using ML/DL

A machine learning and deep learning-based intrusion detection system for detecting **HELLO Flood attacks** in RPL-based IoT networks, inspired by the DETONAR research framework.

## Overview

IoT networks using RPL (Routing Protocol for Low-Power and Lossy Networks) are vulnerable to routing attacks that disrupt communication and exhaust node resources.

This project focuses on detecting the **HELLO Flood attack**, where a malicious node floods the network with fake control (DIO) messages, causing:

- Network congestion  
- Energy depletion  
- Routing instability  
- Denial of Service (DoS)

## Objective

To build and evaluate a robust attack detection pipeline using:

- Machine Learning (ML)
- Deep Learning (DL)
- Unsupervised Anomaly Detection

while addressing **real-world challenges like class imbalance and temporal behavior**.

## Key Features

- End-to-end ML pipeline for IoT intrusion detection  
- Comparative analysis of multiple models  
- Implementation of multiple data balancing techniques  
- Time-aware detection using sequence models  
- Evaluation using real-world inspired dataset  

## Methodology

### 1. Data Preprocessing
- Missing value handling  
- Label encoding for categorical features  
- Feature scaling using StandardScaler  

### 2. Exploratory Data Analysis
- Correlation analysis  
- Class imbalance inspection  

### 3. Data Balancing Techniques
- Baseline (No SMOTE)  
- SMOTE After Train-Test Split  
- SMOTE Before Train-Test Split  
- Manual Downsampling  

### 4. Models Implemented

#### Supervised Models
- Logistic Regression  
- Random Forest Classifier  
- Multi-Layer Perceptron (MLP)  
- LSTM (PyTorch)  
- GRU (PyTorch)  

#### Unsupervised Model
- Isolation Forest  

## Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

## Key Results

- **Random Forest** achieved the most stable and highest performance across all techniques  
- **Isolation Forest** performed strongly even without labeled training data  
- **SMOTE Before Split** provided the most consistent performance  
- **Deep Learning models (LSTM/GRU)** required larger datasets for optimal results  

## Repository Structure
├── notebooks/
│ ├── 01_baseline_no_smote.ipynb
│ ├── 02_smote_after_split.ipynb
│ ├── 03_smote_before_split.ipynb
│ ├── 04_manual_downsampling.ipynb
│ └── 05_comparative_analysis.ipynb
│
├── reports/
│ ├── proposal_report.pdf
│ └── final_report.pdf
│
└── README.md

## Project Highlights

- Tackles **real-world IoT security problem**
- Demonstrates **practical ML engineering workflow**
- Compares **ML vs DL vs Unsupervised approaches**
- Handles **data imbalance (critical in cybersecurity datasets)**

## Future Improvements

- Real-time streaming-based detection  
- Integration with network monitoring tools  
- Deployment as an IDS module  
- Extension to other RPL attacks (Sybil, Blackhole, Rank attacks)

## References

- DETONAR: Detection of Routing Attacks in RPL-Based IoT  
