🔬 Breast Cancer Prediction — KNN Classifier
A machine learning project that predicts whether a breast tumor is Malignant (Cancerous) or Benign (Safe) based on 30 tumor measurements.

📌 Problem Statement
Given clinical measurements of a breast tumor, predict whether it is:

1 → Malignant ⚠️ (Cancerous)
0 → Benign ✅ (Safe)


📊 Dataset
DetailInfoSourceKaggle — KNN Algorithm DatasetRows569 patientsFeatures30 numerical measurementsTargetdiagnosis (M or B)Missing ValuesNone
Key Features:

radius_mean — average tumor size
texture_mean — surface texture
area_mean — tumor area
concavity_mean — concavity of tumor edges
symmetry_mean — tumor symmetry


🤖 Model Used
K-Nearest Neighbors (KNN)

Finds K most similar patients from training data
Majority vote determines prediction
Distance metric: Euclidean

New Patient → Calculate distance to all training patients
           → Pick K nearest neighbors
           → Majority vote → Malignant or Benign

⚙️ Steps Followed

Load and explore dataset
Drop id column (not useful for ML)
Convert diagnosis → M=1, B=0
Split into train (80%) and test (20%)
Apply MinMaxScaler (scaling is critical for KNN!)
Train KNN model with K=5
Evaluate with confusion matrix and classification report

Accuracy:96%

🛠️ Libraries Used
pandas
numpy
scikit-learn

📁 Files
01_KNN_Cancer_Prediction/
├── KNN_Cancer.ipynb
├── dataset.csv
└── README.md

Built while learning Scikit-Learn — Ryan & Matt Data Science playlist