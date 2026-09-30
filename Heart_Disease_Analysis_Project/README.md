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
     - Lasso Regression (feature selection)
     - Random Forest
     - Logistic Regression (grid-searched, class-weighted)
   - Evaluated models using precision, recall, F1-score, and ROC-AUC, not accuracy alone.
4. **Addressing Imbalance**:
   - Used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset and improve model performance.

## Files
- **`Heart_Disease_Prediction_Analysis.ipynb`**: preprocessing, EDA, and the main Random Forest and Logistic Regression results reported below.
- **`Heart_Disease_Modeling_and_Visualizations.ipynb`**: Lasso feature selection, SMOTE experiments, confusion matrices, and visualizations.
- **`Heart_Disease_Group_Project.ipynb`**: the team's combined notebook.
- **`Heart_Disease_Project_Documentation.pdf`**: project documentation.
- **Dataset**: download from [Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease) (not stored in this repo because of its size).

## Results
Only about 9% of people in the test set (4,296 of 49,203) have heart disease, so a model that always predicts "no" would score about 91% accuracy while missing every patient. The metric that matters is **recall on the heart-disease class**: how many real cases the model catches.

Results on the hold-out test set (`Heart_Disease_Prediction_Analysis.ipynb`):

| Model | Accuracy | Heart-disease precision | Heart-disease recall | ROC-AUC |
|---|---|---|---|---|
| Random Forest (class-weighted) | 90% | 31% | 10% | 0.75 |
| Logistic Regression (class-weighted, tuned) | 74% | 22% | **77%** | **0.83** |

### Key Observations
1. **Random Forest's 90% accuracy is misleading.** It is below the 91% "always no" baseline and catches only 1 in 10 heart-disease cases.
2. **Logistic Regression is the more useful screening model.** It trades overall accuracy for catching 77% of real cases, which is the right trade-off when missing a patient is costlier than a false alarm.
3. **Top predictors:** Lasso identified self-reported General Health as the strongest predictor; Random Forest and Logistic Regression both emphasized AgeCategory, ChestScan, and HadDiabetes.

### Limitation
In the SMOTE experiments, oversampling was applied before the train/test split, so synthetic samples reached the test set and those scores are optimistic. The results in the table above do not use SMOTE. The fix is to split first and apply SMOTE only to the training data.

## Insights
1. Early intervention for high-risk individuals (e.g., smokers, diabetics) can reduce heart disease risk.
2. Sleep time and physical activity are critical behavioral factors influencing heart health.
3. For imbalanced medical data, accuracy is the wrong yardstick: recall on the heart-disease class should drive model choice.

## Future Work
- Expand the analysis to include external datasets for better generalization.
- Explore deep learning techniques to capture complex feature interactions.
- Develop an interactive dashboard to visualize results and provide real-time predictions.

## Tools and Libraries
- **Python**:
  - Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, imbalanced-learn.
- **Jupyter Notebooks**: For EDA, modeling, and visualizations.

## Acknowledgments
- **Team Members**:
  - Yunlong Ou, Yunzhuo Liu, Yuyun Zhen, Te-Hsin Kung, Joshua Liu
- **Dataset Source**: [Kaggle - Personal Key Indicators of Heart Disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
