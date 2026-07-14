# Wine Quality Prediction
A develop ML model to predict the quality of wine (good or bad) based on physiochemical properties

## 🎯 Business Problem

This project aims to develop a machine learning model that predicts wine quality (good or bad) based on physicochemical properties of the wine. By analyzing chemical characteristics such as alcohol content, acidity levels, and sulfate concentrations, the model can help winemakers identify quality factors and improve production processes.

**Key Business Question:** Can we predict wine quality using physicochemical properties, and which factors have the strongest influence on quality?

## 📁 Repository Structure

```
Wine_Quality.ipynb
├── 1. Imports
├── 2. EDA (Exploratory Data Analysis)
├── 3. Data Preprocessing
│   ├── Label Encoding
│   ├── Feature-Target Split
│   └── Train-Test Split
├── 4. Model Development
├── 5. Model Evaluation
└── 6. Results Visualization

data.csv - Wine quality dataset with physicochemical properties
```

## ⚒️ Tools and Programming Languages

- **Language:** Python 3
- **Data Processing:**
  - Pandas (data loading and manipulation)
  - NumPy (numerical operations)
- **Machine Learning:**
  - scikit-learn (RandomForestClassifier, SVC, train_test_split, GridSearchCV)
  - StandardScaler (feature normalization)
  - LabelEncoder (categorical encoding)
- **Model Evaluation:**
  - Confusion Matrix
  - Classification Report
  - Accuracy Score
  - Cross-validation scoring
- **Visualization:** Matplotlib and Seaborn (distribution plots, correlation analysis)

## 🔑 Key Insights & Results

### Dataset Analysis
- **Target Variable:** Wine quality categorized as "good" or "bad"
- **Quality Threshold:** Wines with quality > 6.5 classified as "good", ≤ 6.5 as "bad"
- **Number of Features:** 11 physicochemical properties

### Feature Correlations with Wine Quality
- **Positive Correlations:**
  - Sulphates: Strong positive correlation with wine quality
  - Citric Acid: Moderate positive correlation with wine quality
  - Alcohol Content: Slight positive correlation with wine quality

- **Negative Correlations:**
  - Volatile Acidity: Negative correlation with wine quality
  - Chlorides: Negative correlation with wine quality

### Data Characteristics
- **Class Distribution:** Analyzed before and after binary classification
- **Feature Relationships:** Visualized through bar plots and distribution analysis

### Models Used
1. **Random Forest Classifier:** Ensemble method for robust predictions
2. **Support Vector Machine (SVM):** Kernel-based classifier for high-dimensional data

### Optimization Techniques
- **GridSearchCV:** Hyperparameter tuning to find optimal model parameters
- **Cross-Validation:** Multiple fold validation for robust performance estimation
- **StandardScaler:** Feature normalization for SVM and other distance-based algorithms

### 🏆 Best Model & Performance

**Winning Model:** Support Vector Machine (SVM) with SMOTE + Hyperparameter Tuning

**Key Performance Metrics:**
- **Accuracy:** 91%
- **F1-Macro Score:** 79%
- **Optimization:** GridSearchCV hyperparameter tuning with parameters:
  - C: [0.1, 0.8, 0.9, 1, 1.1, 1.2, 1.3, 1.4]
  - kernel: ['linear', 'rbf']
  - gamma: [0.1, 0.8, 0.9, 1, 1.1, 1.2, 1.3, 1.4]
- **Data Balancing:** SMOTE applied to address class imbalance between good and bad wine classifications
- **Comparison:** Random Forest tested but SVM with optimized hyperparameters achieved superior performance
- **Evaluation:** Confusion matrix and classification report confirm strong prediction capability

### 💡 Business Recommendations
1. Focus on reducing volatile acidity to improve wine quality
2. Increase sulphate levels strategically to enhance quality
3. Optimize citric acid content in production
4. Monitor chloride levels during winemaking process
