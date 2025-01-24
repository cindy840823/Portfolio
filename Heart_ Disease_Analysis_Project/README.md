# Heart Disease Prediction Project

## Overview
This project explores machine learning techniques to predict the likelihood of heart disease based on personal and behavioral health indicators. Using a dataset sourced from Kaggle, we investigate relationships between key risk factors (e.g., smoking, physical activity, BMI) and heart disease prevalence. The project demonstrates data preprocessing, exploratory data analysis, feature engineering, and the development of predictive models.

## Dataset
- **Source**: [Kaggle - Personal Key Indicators of Heart Disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
- **Description**:
  - The dataset contains over 300,000 responses to the CDC's annual Behavioral Risk Factor Surveillance System (BRFSS) survey.
  - **Features**:
    - Demographic attributes: AgeCategory, Sex, Race.
    - Health attributes: BMI, PhysicalActivity, Smoking, Diabetes, SleepTime.
    - Behavioral indicators: AlcoholDrinking, Stroke, MentalHealth.
  - **Target Variable**: `HeartDisease` (Binary: Yes/No)

## Objectives
1. Perform data preprocessing, including handling missing values and encoding categorical variables.
2. Conduct exploratory data analysis (EDA) to identify trends and correlations in health and demographic factors.
3. Train and evaluate machine learning models to predict heart disease risk.
4. Address class imbalance using oversampling techniques (e.g., SMOTE).

## Methodology
1. **Data Preprocessing**:
   - Cleaned the dataset by removing missing values and encoding categorical features.
   - Created new features to capture combined health risk factors.
2. **Exploratory Data Analysis**:
   - Examined distributions of key features like BMI, SleepTime, and Smoking status.
   - Investigated correlations between risk factors and heart disease.
3. **Modeling**:
   - Applied various machine learning algorithms, including:
     - Logistic Regression
     - Decision Trees
     - Random Forest
     - Gradient Boosting (XGBoost)
   - Evaluated models using metrics like accuracy, precision, recall, F1-score, and ROC-AUC.
4. **Addressing Imbalance**:
   - Used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset and improve model performance.

## Files
- **`Heart_Disease_Prediction_Analysis.ipynb`**:
  - Notebook containing data preprocessing, EDA, and insights generation.
- **`Heart_Disease_Modeling.ipynb`**:
  - Notebook focused on training, testing, and evaluating machine learning models.
- **`Heart_Disease_Group_Project_Notebook.ipynb`**:
  - Collaborative notebook summarizing the team's collective analysis and findings.
- **`Heart_Disease_Project_Documentation.docx`**:
  - Detailed documentation of the project, including methodology and results.
- **`data/Heart_Disease_Indicators.csv`**:
  - Dataset containing the personal key indicators of heart disease.
- **`visuals/`**:
  - Contains charts and visualizations:
    - Confusion matrices
    - Feature importance plots
    - Model accuracy comparisons

## Results
### Model Performance
- **Logistic Regression**:
  - Accuracy: 84.6%
  - Precision: 78.5%
  - Recall: 80.2%
  - F1-Score: 79.3%
  - ROC-AUC: 0.87

- **Decision Tree**:
  - Accuracy: 81.3%
  - Precision: 76.8%
  - Recall: 77.9%
  - F1-Score: 77.3%
  - ROC-AUC: 0.84

- **Random Forest**:
  - Accuracy: 88.9%
  - Precision: 83.2%
  - Recall: 85.7%
  - F1-Score: 84.4%
  - ROC-AUC: 0.91

- **XGBoost (Best Model)**:
  - Accuracy: 91.0%
  - Precision: 86.4%
  - Recall: 88.5%
  - F1-Score: 87.4%
  - ROC-AUC: 0.93

### Key Observations
1. **XGBoost** outperformed other models across all metrics, making it the best choice for predicting heart disease.
2. **Random Forest** was a close second, balancing high accuracy with interpretability.
3. **Logistic Regression** provided competitive results with simplicity and interpretability, making it ideal for scenarios requiring explainable models.
4. **Decision Tree** had the lowest performance but highlighted important features, useful for quick insights.

## Insights
1. Early intervention for high-risk individuals (e.g., smokers, diabetics) can reduce heart disease risk.
2. Sleep time and physical activity are critical behavioral factors influencing heart health.
3. Class imbalance techniques like SMOTE improved the sensitivity of the models.

## Future Work
- Expand the analysis to include external datasets for better generalization.
- Explore deep learning techniques to capture complex feature interactions.
- Develop an interactive dashboard to visualize results and provide real-time predictions.

## Tools and Libraries
- **Python**:
  - Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, xgboost, imbalanced-learn.
- **Jupyter Notebooks**: For EDA, modeling, and visualizations.
- **Microsoft Word**: For documentation and reporting.

## Acknowledgments
- **Team Members**:
  - Yunlong Ou, Yunzhuo Liu, Yuyun Zhen, Te-Hsin Kung, Joshua Liu
- **Dataset Source**: [Kaggle - Personal Key Indicators of Heart Disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
