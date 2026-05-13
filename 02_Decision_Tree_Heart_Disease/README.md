🫀 Heart Disease Prediction — Decision Tree Classifier
A machine learning project that predicts whether a patient has heart disease or not based on clinical health measurements.

📌 Problem Statement
Given health measurements of a patient, predict whether they have heart disease:

1 → Has Heart Disease ⚠️
0 → No Heart Disease ✅


📊 Dataset
DetailInfoSourceKaggle — Decision Tree DatasetRows297 patientsFeatures13 health measurementsTargetcondition (0 or 1)Missing ValuesNone
Key Features:
ColumnMeaningagePatient agesex1=Male, 0=FemalecpChest pain type (0-3)trestbpsResting blood pressurecholCholesterol levelthalachMax heart rate achievedexangExercise induced anginacaNumber of major vesselsthalThalassemia type

🤖 Model Used
Decision Tree Classifier

Asks a series of YES/NO questions about patient stats
Follows the path until reaching a final diagnosis
No feature scaling needed!

Patient arrives at ROOT node
      ↓
"Is cp (chest pain) <= 1?"
   YES → next question
   NO  → next question
      ↓
...keeps going until LEAF node
      ↓
Prediction: Heart Disease or Not

⚙️ Steps Followed

Load and explore dataset
Split features (X) and target (y)
Train test split — 80% train, 20% test
Train two Decision Trees and compare:

Tree 1: criterion='gini', no pruning
Tree 2: criterion='entropy', ccp_alpha=0.0001



Compare feature importances
Evaluate with confusion matrix and classification report

🛠️ Libraries Used
pandas
numpy
scikit-learn

📁 Files
02_Decision_Tree_Heart_Disease/
├── Decision_Tree.ipynb
├── heart_cleveland.csv
└── README.md

Built while learning Scikit-Learn — Ryan & Matt Data Science playlist