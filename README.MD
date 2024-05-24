# Heart Disease Prediction

## Project Overview
This project aims to predict whether a person will have heart disease in the next ten years. It specifically tackles the overlooked issue of data imbalance found in previous studies of similar datasets, which often reported misleadingly high accuracy scores. This project corrects data imbalance and leakage, providing a more reliable predictive model.

## Data Source
The dataset is sourced from Kaggle and was previously used without addressing its imbalance issues. This project addresses these issues to ensure more valid results.

- [Heart Disease Prediction Using Logistic Regression - Kaggle Code](https://www.kaggle.com/code/neisha/heart-disease-prediction-using-logistic-regression)
- [Heart Disease Prediction Using Logistic Regression - Kaggle Dataset](https://www.kaggle.com/datasets/dileep070/heart-disease-prediction-using-logistic-regression/code)

## Features of the Project
- **Data Cleaning**: Tackles missing data and outliers. Missing values were imputed based on distribution and outliers were managed according to standard deviation and acceptable range guidelines found online.
- **Data Transformation**: Corrects data imbalance through appropriate transformations and preprocessing techniques, enhancing model accuracy. No string encoding was needed as all features were numerical.
- **Model Training**: Splitting the dataset into training and testing sets to ensure a robust training process.
- **Model Evaluation**: Utilizing tools like confusion matrix and classification report to evaluate model performance on training and test datasets.
- **Leakage Correction**: Identified and corrected data leakage, which is crucial for maintaining the integrity of the model's predictive power.

## Technologies Used
- Python
- Pandas, NumPy for data manipulation
- Scikit-learn for modeling and data preprocessing

## Setup and Installation
1. Clone the repository:
2. Install required Python packages:
3. Run the Jupyter Notebook:

## Results
The project successfully addresses the imbalance in the dataset, which had previously led to inflated accuracy scores in other studies. By applying appropriate preprocessing methods, the model now reflects a more accurate prediction of heart disease risk, with robustness against data leakage and imbalance. Key metrics improved significantly post-correction, underscoring the importance of handling data quality issues in predictive modeling.

## Results and Importance of Data Leakage Correction

### Confusion Matrix Analysis
The results of the confusion matrix before and after data leakage correction illustrate the significant impact of addressing this issue:

**Before Correction:**
- **True Negatives (TN):** 657
- **False Positives (FP):** 3
- **False Negatives (FN):** 110
- **True Positives (TP):** 2

The model before correction showed a high number of false negatives and an extremely low number of true positives, indicating a tendency to under-predict the positive class (presence of heart disease). This was likely due to the model being trained on imbalanced data, where the leakage led to overfitting on the negative outcomes.

**After Correction:**
- **True Negatives (TN):** 643
- **False Positives (FP):** 28
- **False Negatives (FN):** 7
- **True Positives (TP):** 641

After correcting the data leakage, the model exhibits a more balanced performance between the classes. The number of true positives drastically increased from 2 to 641, and false negatives decreased significantly from 110 to 7, showing the model's improved ability to identify the positive class correctly.

### Impact of Data Leakage Correction
Correcting data leakage fundamentally changed the predictive dynamics of the model:
- **Reduced Bias:** Initially, the model was biased towards predicting negatives, which could be misleading in a clinical diagnosis scenario.
- **Improved Sensitivity:** The sensitivity (or recall) of the model for the positive class improved dramatically, indicating a lower chance of missing out on patients who actually have heart disease.
- **Enhanced Generalization:** The model now generalizes better to unseen data, reducing the risk of errors in real-world applications.

This correction highlights the necessity of proper data handling and preprocessing in predictive modeling, especially in medical applications where accurate predictions can significantly impact patient outcomes.

## Conclusion
The correction of data leakage in this heart disease prediction project underscores the importance of rigorous data quality and preprocessing protocols in developing reliable and effective predictive models, particularly in fields like healthcare where the stakes are high.


## How to Use
- Follow the Jupyter Notebook to see each step of data preprocessing, model training, and evaluation.
- Modify parameters and methods to test different approaches to data handling and model configuration.


