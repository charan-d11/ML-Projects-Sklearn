🍷 Wine Quality Prediction — Random Forest Classifier
A machine learning project that predicts whether a white wine is Good Quality or Poor Quality based on its chemical properties.

📌 Problem Statement
Given chemical measurements of a white wine, predict its quality:

1 → Good Wine ✅ (quality score ≥ 7)
0 → Poor Wine ❌ (quality score < 7)


📊 Dataset
DetailInfoSourceKaggle — abdelazizsami/wine-qualityRows4,898 winesFeatures11 chemical propertiesTargetquality (converted to binary)Missing ValuesNoneFile SeparatorSemicolon ;
Features:
ColumnMeaningfixed acidityNon-volatile acid levelvolatile acidityAcetic acid amountcitric acidFreshness indicatorresidual sugarSugar after fermentationchloridesSalt contentfree sulfur dioxideFree SO2 leveltotal sulfur dioxideTotal SO2 leveldensityWine densitypHAcidity levelsulphatesPreservative levelalcoholAlcohol percentage

🤖 Model Used
Random Forest Classifier

Builds multiple Decision Trees on random subsets of data
Each tree votes → majority vote = final prediction
Much better than single Decision Tree!

4898 wines
    ↓
Build 100 diverse Decision Trees
Each on random bootstrap sample
    ↓
New wine → all 100 trees vote
    ↓
Majority vote → Good or Poor wine

⚙️ Steps Followed

Load dataset with sep=';' (semicolon separated!)
Convert quality score to binary:

python   df['quality'] = df['quality'].apply(lambda x: 1 if x >= 7 else 0)

Split features (X) and target (y)
Train test split — 80% train, 20% test
Train two Random Forests and compare:

Forest 1: n_estimators=100 (default)
Forest 2: n_estimators=1000, criterion='entropy'


Compare feature importances
Evaluate accuracy, confusion matrix


📈 Results
ModelAccuracyForest 1 (100 trees)88%,Forest 2 (1000 trees)98% ✅
Key Finding:

More trees did NOT improve accuracy — 100 trees was enough for this dataset!


🛠️ Libraries Used
pandas
numpy
scikit-learn

📁 Files
03_Random_Forest_Wine_Quality/
├── Random_Forest_Wine.ipynb
├── winequality-white.csv
└── README.md

Built while learning Scikit-Learn — Ryan & Matt Data Science playlist