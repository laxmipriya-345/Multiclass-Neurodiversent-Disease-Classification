Multi-Class Neurodivergent Disease Classification
AutoML + Federated Learning + Optuna
Project Overview

This project presents an intelligent and privacy-preserving machine learning framework for multi-class classification of neurodivergent / neurodegenerative diseases, specifically:

Alzheimer’s Disease (AD)

Parkinson’s Disease (PD)

Amyotrophic Lateral Sclerosis (ALS)

Healthy Control (Optional)

The system integrates AutoML, Federated Learning, and Optuna-based hyperparameter optimization to achieve high classification performance while preserving patient data privacy.

 Objectives

Develop a multi-class disease classification model instead of multiple binary classifiers

Preserve data privacy using Federated Learning

Automatically optimize models using AutoML + Optuna

Achieve robust and scalable performance across distributed healthcare datasets

🧪 Diseases Considered
Class Label	Disease
0	Healthy Control
1	Alzheimer’s Disease
2	Parkinson’s Disease
3	ALS
🧩 Key Technologies Used

Python

AutoML frameworks (custom pipeline / AutoGluon / H2O / sklearn-based)

Federated Learning (Flower / FedAvg strategy)

Optuna (Hyperparameter Optimization)

Scikit-learn

PyTorch / TensorFlow

NumPy, Pandas

Matplotlib, Seaborn

🏗️ System Architecture
+--------------------+
| Client 1 (Hospital)|
| Alzheimer’s Data   |
+--------------------+

+--------------------+
| Client 2 (Clinic)  |
| Parkinson’s Data   |
+--------------------+

+--------------------+
| Client 3 (Lab)     |
| ALS Data           |
+--------------------+

        ⬇ Federated Learning (FedAvg)

+----------------------------------+
| Central Server (No Raw Data)     |
| Global Model Aggregation         |
+----------------------------------+

🔁 Methodology
1️⃣ Data Preprocessing

Data cleaning and normalization

Handling missing values

Feature encoding and scaling

Label encoding for multiclass classification

2️⃣ AutoML Pipeline

Automatic model selection:

Logistic Regression

Random Forest

XGBoost

SVM

Neural Networks

Automatic feature selection

Cross-validation based evaluation

3️⃣ Hyperparameter Optimization (Optuna)

Optuna is used to:

Tune learning rate, depth, number of estimators

Optimize batch size and epochs

Minimize validation loss

Maximize macro-F1 score

study = optuna.create_study(direction="maximize")
study.optimize(objective, n_trials=50)

4️⃣ Federated Learning

Distributed training across multiple clients

No raw patient data is shared

Model weights are aggregated using Federated Averaging (FedAvg)

Supports real-world healthcare deployment

5️⃣ Multi-Class Classification

Softmax-based output layer

Handles class imbalance

Supports extensibility to new diseases

 Evaluation Metrics

Accuracy

Precision (Macro & Micro)

Recall

F1-Score

Confusion Matrix

ROC-AUC (One-vs-Rest)

📈 Results

Improved generalization using Federated Learning

Optimal hyperparameters discovered using Optuna

Reduced overfitting through AutoML model selection

Secure and privacy-preserving training

(Exact results depend on dataset used)

🗂️ Project Structure
├── data/
│   ├── client1_alzheimer/
│   ├── client2_parkinson/
│   └── client3_als/
│
├── preprocessing/
│   └── preprocess.py
│
├── automl/
│   └── automl_pipeline.py
│
├── federated/
│   ├── client.py
│   └── server.py
│
├── optuna/
│   └── optuna_search.py
│
├── evaluation/
│   └── metrics.py
│
├── main.py
└── README.md

 Privacy & Security

No centralized data storage

Patient data remains at local clients

Only encrypted model updates are transmitted

 How to Run
# Install dependencies
pip install -r requirements.txt

# Start federated server
python federated/server.py

# Start clients
python federated/client.py

 Applications

Clinical decision support systems

Early diagnosis of neurodegenerative diseases

Privacy-aware healthcare AI

Research in distributed medical AI

 Limitations

Dataset heterogeneity across clients

Limited public ALS datasets

Communication overhead in federated training

 Future Work

Multimodal learning (MRI + speech + EMG)

Explainable AI (SHAP, LIME)

Secure aggregation & differential privacy

Integration with real hospital systems

👩‍💻 Author
Laxmipriya Rout
AI / ML Enthusiast | Healthcare AI Research

