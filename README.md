Neurodivergent conditions such as Autism Spectrum Disorder (ASD), Parkinson’s Disease, and Amyotrophic Lateral Sclerosis (ALS) involve complex patterns in clinical and behavioral data. Early detection and monitoring are crucial, but patient datasets are often distributed across hospitals or research centers and contain sensitive information.

This project uses tabular CSV datasets for these conditions and combines AutoML, Federated Learning, and Optuna to build accurate and privacy-preserving predictive models:

Datasets: Structured CSV data with features like patient demographics, clinical assessments, neurological tests, and behavioral scores for Autism, Parkinson’s, and ALS.

AutoML: Automatically explores and selects the best machine learning models (e.g., Random Forest, XGBoost, LightGBM, Neural Networks) and preprocessing pipelines for optimal performance.

Optuna: Performs automated hyperparameter optimization to fine-tune each model for better predictive accuracy.

Federated Learning: Enables collaborative model training across multiple institutions without sharing raw patient data. Each site trains the model locally, and only model updates are aggregated centrally, preserving privacy and complying with data protection regulations.

Outcome: Predictive models can assess disease presence, severity, or progression, supporting early intervention and personalized treatment strategies.

Key Advantages:

Privacy-preserving learning on sensitive healthcare data.

Automated model and hyperparameter selection reduces manual effort.

Utilizes distributed, heterogeneous data for improved generalization.

Scalable and suitable for multiple neurodivergent disorders simultaneously.

This project demonstrates a state-of-the-art AI approach for tabular healthcare data, combining automation, optimization, and federated learning to improve predictive analytics for neurodivergent diseases.
