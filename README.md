# Project Sentinel: A CAI-Powered UEBA Platform for Fraud Detection


This repository contains a runnable Python proof-of-concept for **Project Sentinel**, a next-generation fraud detection platform designed for a bank hackathon. The project demonstrates how a multi-layered AI approach can identify complex fraud patterns in real-time, reduce false positives, and provide clear, actionable insights.

## The Problem
Traditional, rule-based fraud detection systems are failing. They struggle to keep up with sophisticated threats like compromised credentials and organized mule account networks. This results in:
-   **Financial Losses** from missed fraudulent transactions.
-   **Poor Customer Experience** due to a high number of legitimate transactions being incorrectly blocked (false positives).
-   **High Operational Costs** from manually reviewing thousands of false alarms.

## The Solution: Project Sentinel
Project Sentinel is a smart, adaptive engine that moves beyond static rules. It uses a **Cognitive AI** and **User & Entity Behaviour Analytics (UEBA)** approach to understand the *context* behind every transaction.

### Key Features Demonstrated in this Code:
-   **Multi-Layered AI Analysis:** Combines anomaly detection (Isolation Forest), predictive modeling (XGBoost), and conceptual graph analytics to generate a single, highly accurate risk score.
-   **360-Degree Behavioral Context:** Enriches transaction data with behavioral features (like recent device changes) to build a more complete picture of user activity.
-   **Clear, Structured Reporting:** The output is designed to be a professional "Analysis Report" that clearly explains the engine's decision-making process for each transaction.

---

## Live Demonstration: Sample Output
The script produces a detailed report for each transaction, showing the intelligence at work. Here is the output for a high-risk transaction:

```
======================================================================
    ANALYSIS REPORT FOR TRANSACTION ID: TXN2002
======================================================================

--- Stage 1: Feature Engineering ---
  Transaction Amount            : $9500.00
  Hour of Day                   : 3:00
  Is New Beneficiary            : True
  Recent Device Changes         : 3

--- Stage 2: Model Inference ---
  Anomaly Score (Isolation Forest): -0.1118 (Note: Negative is more anomalous)
  Fraud Probability (XGBoost)   : 0.9850 (Note: Higher indicates fraud)
  Graph Analysis Alert          : No links to known fraud networks found.

--- Stage 3: Risk Synthesis ---
  XGBoost Contribution          : 78.80 / 80.00
  Anomaly Contribution          : 2.24 / 20.00
  Graph Network Penalty         : 0.00
  FINAL RISK SCORE (0-100)      : 81

--- Stage 4: Final Decision ---
  Recommended Action            : BLOCK & ALERT
======================================================================
```

---

## How to Run This Project

### Prerequisites
- Python 3.7+

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME
```

### 2. Install Dependencies
No `requirements.txt` file is needed. Simply run this single command to install all required libraries:
```bash
pip install pandas numpy scikit-learn xgboost```

### 3. Run the Engine
Execute the `Project_Sentinel.py` script to see the live analysis of the sample transactions.
```bash
python Project_Sentinel.py
```

---

## Technology Stack

-   **Language:** Python 3
-   **Core Libraries:**
    -   `scikit-learn`: For the Isolation Forest anomaly detection model.
    -   `xgboost`: For the high-performance gradient boosting fraud prediction model.
    -   `pandas` & `numpy`: For efficient data manipulation.
-   **Key Algorithms Demonstrated:**
    1.  **Unsupervised Anomaly Detection:** Isolation Forest
    2.  **Supervised Fraud Prediction:** XGBoost (Extreme Gradient Boosting)
    3.  **Graph Analytics (Conceptual):** A risk-boost system simulating the detection of mule account networks.
