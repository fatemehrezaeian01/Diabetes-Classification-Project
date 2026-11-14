# Evaluating Machine Learning Methods for Imbalanced Classification

## Project Overview

This project investigates the performance of different machine learning algorithms for diabetes classification using the Pima Indians Diabetes Database.

The main objective is to compare standard and class-weighted classification models and evaluate how class imbalance affects predictive performance.

The project focuses on data preprocessing, model development, cross-validation, performance evaluation, and feature importance analysis.

## Dataset

The project uses the Pima Indians Diabetes Database, which contains 768 observations and 9 columns:
  •	8 predictor features
  •	1 target variable (Outcome)

The target variable indicates whether a patient has diabetes:
  •	0: No diabetes
  •	1: Diabetes

The dataset contains 500 negative cases (65.1%) and 268 positive cases (34.9%), indicating a moderately imbalanced target distribution.

## Methods and Workflow

The project follows these main steps:
    1.	Exploratory Data Analysis (EDA)
	•	Dataset structure and descriptive statistics
	•	Target variable distribution
	•	Investigation of zero values in selected medical measurement features
	2.	Data Preprocessing
	•	Replacement of potentially invalid zero values with missing values
	•	Median imputation
	•	Use of machine learning pipelines to reduce data leakage
	3.	Model Development
	•	Logistic Regression
	•	Balanced Logistic Regression
	•	Decision Tree
	•	Balanced Decision Tree
	•	Random Forest
	•	Balanced Random Forest
	4.	Model Evaluation
	•	Stratified 5-fold cross-validation
	•	Accuracy
	•	Precision
	•	Recall
	•	F1-score
	•	ROC-AUC
	5.	Additional Analysis
	•	ROC curve comparison
	•	Precision-Recall curve analysis
	•	Decision threshold analysis
	•	Feature importance analysis using Random Forest

## Cross-Validation Results

The following results represent the mean performance of each model using stratified 5-fold cross-validation on the training data.

1. Logistic Regression
  •	Accuracy: 0.788
  •	Precision: 0.764
  •	Recall: 0.575
  •	F1-score: 0.655
  •	ROC-AUC: 0.843

3. Balanced Logistic Regression
  •	Accuracy: 0.762
  •	Precision: 0.649
  •	Recall: 0.701
  •	F1-score: 0.672
  •	ROC-AUC: 0.844

4. Decision Tree
  •	Accuracy: 0.673
  •	Precision: 0.531
  •	Recall: 0.580
  •	F1-score: 0.552
  •	ROC-AUC: 0.651

5. Balanced Decision Tree
  •	Accuracy: 0.673
  •	Precision: 0.532
  •	Recall: 0.533
  •	F1-score: 0.532
  •	ROC-AUC: 0.640

6. Random Forest
  •	Accuracy: 0.761
  •	Precision: 0.690
  •	Recall: 0.575
  •	F1-score: 0.626
  •	ROC-AUC: 0.816

7. Balanced Random Forest
  •	Accuracy: 0.764
  •	Precision: 0.654
  •	Recall: 0.701
  •	F1-score: 0.675
  •	ROC-AUC: 0.820

## Key Findings
  •	Logistic Regression achieved the highest mean accuracy and precision.
  •	Balanced Logistic Regression and Balanced Random Forest achieved higher mean recall than their standard counterparts.
  •	Balanced Random Forest achieved the highest mean F1-score among the six evaluated models.
  •	Class weighting improved recall for Logistic Regression and Random Forest, although this came with trade-offs in other evaluation metrics.
  •	Feature importance analysis identified Glucose as the most influential feature in the standard Random Forest model, followed by BMI, DiabetesPedigreeFunction, and Age.

These findings demonstrate that model selection depends on the evaluation metric and the priorities of the classification task.

## Project Structure
```text
Diabetes-Classification-Project/
│
├── medical_ml_project.ipynb
└── README.md
```

## Technologies Used
  •	Python
  •	NumPy
  •	Pandas
  •	Matplotlib
  •	Seaborn
  •	Scikit-learn
  •	Jupyter Notebook

## How to Run
1.Clone or download this repository.
2.Install the required Python libraries:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

4.Open the project notebook:
```bash
jupyter notebook medical_ml_project.ipynb
```
5.Run the notebook cells from top to bottom.

## Limitations
   •	The dataset is relatively small and contains a moderately imbalanced target variable.
   •	The models use default or basic configurations rather than extensive hyperparameter optimization.
   •	Feature importance represents the model’s internal use of features and does not establish causation or clinical significance.
   •	The models have not been clinically validated and should not be used for medical diagnosis.

## Disclaimer

This project is intended for educational and experimental purposes only. The developed models are not medical diagnostic tools and should not be used to make clinical decisions.
  
