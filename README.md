# Heart Failure Prediction through Machine Learning

## Project Overview

Heart disease is one of the leading causes of death worldwide, and it has affected my family personally. My dad has been a smoker for over 30 years, and witnessing the impact it has had on his heart health inspired me to explore how machine learning and data science, fields I am passionate about, can be applied in the medical domain. This project aims to leverage machine learning techniques to predict the risk of heart failure, using a dataset that includes various patient attributes.

### Problem Statement

Cardiovascular diseases (CVDs) account for approximately 17.9 million deaths globally each year, which translates to 31% of all global deaths. Heart failure, a common consequence of CVDs, poses a significant health risk, especially for individuals with pre-existing conditions such as hypertension, diabetes, or a history of smoking, like my father. Early detection and management of such conditions are crucial, and this is where machine learning can play a pivotal role. By analyzing patient data, we can classify individuals based on their risk of heart failure, allowing for timely intervention and treatment.

### Project Aim

The goal of this project is to build a machine learning model that can predict whether a patient is prone to heart failure based on a combination of numerical and categorical features. The dataset used in this project comprises 11 key attributes related to heart health, gathered from five different heart disease datasets. This project not only seeks to achieve high accuracy but also aims to interpret the medical significance of the features that contribute to the predictions.

### Dataset and Attributes

The dataset is a combination of five distinct heart disease datasets, making it one of the most comprehensive resources for heart disease prediction with 918 unique observations after cleaning. The dataset includes the following attributes:

- **Age**: Age of the patient
- **Sex**: Gender of the patient (Male/Female)
- **ChestPainType**: Type of chest pain experienced
- **RestingBP**: Resting blood pressure in mm Hg
- **Cholesterol**: Serum cholesterol in mg/dl
- **FastingBS**: Fasting blood sugar (1 if >120 mg/dl, 0 otherwise)
- **RestingECG**: Resting electrocardiogram results (Normal, ST, LVH)
- **MaxHR**: Maximum heart rate achieved
- **ExerciseAngina**: Presence of exercise-induced angina (Yes/No)
- **Oldpeak**: ST depression induced by exercise relative to rest
- **ST_Slope**: The slope of the peak exercise ST segment

The target variable is **HeartDisease**, which indicates the presence (1) or absence (0) of heart disease.

---

## Exploratory Data Analysis (EDA)

### Insights from EDA

Through an in-depth exploratory data analysis, the dataset reveals certain patterns that correlate with heart disease:

- **Age**: Patients between 50-60 years are at the highest risk of heart failure.
- **Sex**: Males are more prone to heart disease than females.
- **Chest Pain**: The presence of asymptomatic chest pain (ASY) strongly correlates with heart disease.
- **Blood Pressure & Cholesterol**: Resting blood pressure levels between 120-140 mm Hg and cholesterol levels between 160-340 mg/dl are significant indicators.
- **Fasting Blood Sugar**: High fasting blood sugar is a critical risk factor.
- **Exercise Angina & Max Heart Rate**: Exercise-induced angina and a maximum heart rate between 120-160 bpm are crucial features.
  
This analysis helped guide feature engineering decisions and informed the choice of machine learning models for this project.

---

## Feature Engineering

To optimize the predictive power of our models, I performed:

- **One-hot encoding** for categorical variables like Chest Pain Type, RestingECG, and ST_Slope, ensuring that each category is treated independently by the algorithm.
- **Data Scaling** for continuous features like Age, RestingBP, Cholesterol, and MaxHR to ensure that they are normalized or standardized as per the distribution. For instance, Oldpeak was normalized due to its skewed distribution, while others like Age and Cholesterol were standardized.

---

## Machine Learning Models

Several machine learning algorithms were tested for their effectiveness in predicting heart disease, including:

### 1. **Logistic Regression**
   - **Accuracy**: 84.54%
   - **Cross-Validation Score**: 91.27%
   - **ROC AUC Score**: 84.93%

### 2. **Random Forest Classifier**
   - **Accuracy**: 88.89%
   - **Cross-Validation Score**: 92.33%
   - **ROC AUC Score**: 88.68%

### 3. **K-Nearest Neighbors (KNN) Classifier**
   - **Accuracy**: 85.02%
   - **Cross-Validation Score**: 88.57%
   - **ROC AUC Score**: 85.50%

### 4. **Support Vector Classifier (SVC)**
   - **Accuracy**: 82.61%
   - **Cross-Validation Score**: 90.85%
   - **ROC AUC Score**: 83.10%

The **Random Forest Classifier** demonstrated the highest performance across all metrics, with a balance of accuracy, precision, and recall, making it the optimal model for predicting heart failure in this dataset.

---

## Results and Conclusion

The final model, a Random Forest Classifier, achieved an accuracy of 88.89% with a ROC AUC score of 88.68%, demonstrating its robustness in predicting heart disease. This project highlighted the power of machine learning in the medical field, showcasing how data can be leveraged to make predictions that could potentially save lives.

For me, this project was not just an academic exercise but a deeply personal one. Seeing my father struggle with heart health motivated me to explore the intersection of data science and healthcare. I hope that one day, machine learning models like this could be applied in real-world clinical settings, offering doctors and patients an early warning system for heart disease.