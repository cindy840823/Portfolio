# Binary Classification Project with PCA

## Overview
This project explores the design and evaluation of four binary classification algorithms:
1. **Linear Discriminant Analysis (LDA)**
2. **Decision Tree**
3. **k-Nearest Neighbors (kNN)**
4. **Support Vector Machine (SVM)**

Additionally, the project evaluates the impact of **Principal Component Analysis (PCA)** on classifier performance by reducing the dimensionality of the features.

## Objectives
- Train classifiers using original features and evaluate their type 1 and type 2 error rates.
- Apply PCA to reduce dimensionality and compare classifier performance with the reduced features.

## Dataset
- **Training Data**: `TrainingData.csv` (900 samples, 27 features + label)
- **Testing Data**: `TestingData.csv` (400 samples, 27 features + label)
- **Features**: Includes attributes like Age, Annual Income, etc.
- **Labels**: LoanApproved (0: Approved, 1: Denied)

## Methods
### Part 1: Classifiers with Original Features
- **Linear Discriminant Analysis (LDA)**:
  - Projected samples onto a suitable direction for classification.
  - Evaluated type 1 and type 2 error rates for various thresholds.
- **Decision Tree**:
  - Designed using Gini Impurity and Information Gain.
- **k-Nearest Neighbors (kNN)**:
  - Evaluated for \(k = 1, 3, 5, 10\).
- **Support Vector Machine (SVM)**:
  - Implemented with a soft margin due to non-linearly separable data.

### Part 2: Classifiers with PCA Features
- Applied PCA to reduce the original 27 features to \(K = 5, 10, 15\).
- Designed and evaluated:
  - kNN classifiers with reduced features.
  - SVM classifiers with reduced features.
- Compared performance with classifiers using original features.

## Results
- **LDA**:
  - Plotted type 1 and type 2 error rates as a function of the threshold.
- **Decision Tree**:
  - Provided decision rules and evaluated error rates.
- **kNN and SVM with PCA**:
  - Showed the impact of reduced dimensionality on classifier performance.

## Tools
- **Programming Language**: Python
- **Libraries**: scikit-learn, numpy, pandas, matplotlib, seaborn

## Files
- `Data603_Project_1.ipynb`: Contains code and analysis.
- `data/TrainingData.csv`: Training dataset.
- `data/TestingData.csv`: Testing dataset.
- `visuals/`: Includes plots and charts generated during the analysis.

## Insights
- PCA significantly reduces computational complexity while maintaining accuracy for kNN and SVM.
- The optimal number of principal components depends on the classifier and dataset characteristics.

## Future Work
- Explore additional classifiers like Random Forest or Gradient Boosting.
- Test on larger, more diverse datasets to validate findings.

## References
- Course: **Principle of Machine Learning (MSML 603)**, UMD - College Park
- Instructor: **Professor Richard J. La**
