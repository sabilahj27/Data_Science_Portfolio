# Heart Disease Prediction

This project is a machine learning application to predict whether a person is likely to have heart disease based on medical data from the **UCI Heart Disease Dataset**. The model predicts binary outcomes: whether a person is **healthy** (0) or has **heart disease** (1).

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Modeling Process](#modeling-process)
- [Model Performance](#model-performance)
- [Usage](#usage)
- [Future Work](#future-work)

## Project Overview
This project applies various machine learning models to predict heart disease presence based on patient data. The final model is a **Neural Network** tuned for better performance, with accuracy improved after hyperparameter tuning. The model distinguishes between healthy individuals and those at risk of heart disease.

## Dataset
The dataset used is the **UCI Heart Disease Dataset**, which contains 303 instances with 14 attributes. The target variable is the presence of heart disease:
- 0: Healthy (no heart disease)
- 1: Heart disease present (original labels 1-4 merged into 1).

### Features
The features used in this dataset include:
- **Age**: Age of the patient
- **Sex**: Gender of the patient (1 = male, 0 = female)
- **CP**: Chest pain type (4 values)
- **Trestbps**: Resting blood pressure
- **Chol**: Serum cholesterol level
- **Fbs**: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- **Restecg**: Resting electrocardiographic results (values 0, 1, 2)
- **Thalach**: Maximum heart rate achieved
- **Exang**: Exercise induced angina (1 = yes, 0 = no)
- **Oldpeak**: ST depression induced by exercise relative to rest
- **Slope**: Slope of the peak exercise ST segment
- **Ca**: Number of major vessels (0-3) colored by fluoroscopy
- **Thal**: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect)

## Modeling Process
The project includes the following steps:
1. **Data Preprocessing**: Cleaning and normalizing data.
2. **Exploratory Data Analysis (EDA)**: Visualizing distributions, relationships, and identifying outliers.
3. **Feature Selection**: Using **ANOVA** to select important features.
4. **Model Building**: Comparing multiple models such as:
   - **Logistic Regression**
   - **Random Forest**
   - **XGBoost Classification**
   - **Neural Network**
5. **Model Tuning**: Hyperparameter tuning using **Grid Search**, ensuring consistent results with **random_state**.

## Model Performance
- **Before Tuning**:
   - Accuracy: 0.89
   - Precision: 0.93
   - Recall: 0.84
   - F1-Score: 0.89

- **After Tuning**:
   - Accuracy: 0.92
   - Precision: 0.94
   - Recall: 0.91
   - F1-Score: 0.92

Neural Network was chosen as the final model due to its consistent performance across all metrics and its superior AUC-ROC score of 0.96.

## Usage
To run this program, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/sabilahj27/data_science_portfolio.git
    cd data_science_portfolio/Heart_Disease_Prediction

2. Install dependencies:
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn xgboost

3. Run the notebook or script to train the model: \
    You can either open the **Google Colab/Jupyter Notebook** file (`Heart_disease_prediction.ipynb`).

4. Input new patient data for prediction: \
    Enter new values interactively for features like age, cholesterol, heart rate, etc., to predict if a patient has heart disease or not.

## Future Work
- Improve model by testing more advanced hyperparameter tuning techniques (e.g., Bayesian optimization).
- Explore additional feature engineering techniques to capture more complex relationships.
- Implement a web-based or mobile interface for real-time heart disease predictions.