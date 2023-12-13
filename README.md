# Diabetes-Prediction-using-Machine-Learning-Classification
# Introduction
Diabetes is one of the common health problems that affect millions of people globally. It is characterised by an increased in the blood glucose level caused by insufficient insulin production. Late detection of this diseases can increase the risk of heart attack, cancer, kidney damage, blindness, and other illnesses. Diabetes prediction is important as it helps for early detection of the disease. A challenging task is making early prediction and diagnosis of diabetes. As a result diabetes disease prediction requires an efficient and accurate method. If the diseases can be predicted accurately, prompt action and measures can be taken to prevent or manage it effectively. This can lead to better health outcomes. 
# Objective
The objective of the dataset is to diagnostically predict whether a patient has diabetes
based on certain diagnostic measurements included in the dataset.
# Description of the dataset
This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases.  Several constraints were placed
on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage. The dataset consist of 769 records and 11 features. The dataset is stored in CSV file. it consist of several independent variables (several medical predictor variables) and only one target dependent variable (Outcome). The features are:
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome
# Data Prepartation/Cleaning
- Data loading/inspection
- Zero values in columns such as bloodpressure, BMI and skin thickness were replace with average values.
- Dropping duplicate values
- Deleting redundant columns
# Exploratory Data Analysis
Exploratory data analysis were performed before training the data. Bar Chart of the value counts for the "Outcome" column to calculate the relative frequencies of the classes was created. This shows the relative proportion of diabetes and non diabetes.


