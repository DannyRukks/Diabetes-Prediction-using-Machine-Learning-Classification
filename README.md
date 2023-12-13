# Diabetes-Prediction-using-Machine-Learning-Classification

# Table of Contents
- [Introduction](#introduction)
- [Objective](#objective)
- [Description of the dataset](#description-of-the-dataset)
- [Data Prepartation and Cleaning](#data-prepartation-and-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Classifier Models](#classifier-models)
- [Best Performing Model](#best-performing-model)
- [Key Findings and Insights](#key-findings-and-insights)
- [Recommendations](#recommendations)

# Introduction
Diabetes is one of the common health problems that affect millions of people globally. It is characterised by an increased in the blood glucose level caused by insufficient insulin production. Late detection of this diseases can increase the risk of heart attack, cancer, kidney damage, blindness, and other illnesses. Diabetes prediction is important as it helps for early detection of the disease. A challenging task is making early prediction and diagnosis of diabetes. As a result diabetes disease prediction requires an efficient and accurate method. If the diseases can be predicted accurately, prompt action and measures can be taken to prevent or manage it effectively. This can lead to better health outcomes. 
# Objective
The objective of the dataset is to diagnostically predict whether a patient has diabetes based on certain diagnostic measurements included in the dataset.
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
# Data Prepartation and Cleaning
- Data loading/inspection
- Zero values in columns such as bloodpressure, BMI and skin thickness were replace with average values.
- Dropping duplicate values
- Deleting redundant columns
# Exploratory Data Analysis
Exploratory data analysis were performed before training the dataset. Bar Chart of the value counts for the "Outcome" column to calculate the relative frequencies of the classes was created. This shows the relative proportion of diabetes and non diabetes.

![Bar chart](https://github.com/DannyRukks/Diabetes-Prediction-using-Machine-Learning-Classification/assets/97890440/621982fb-b610-4b33-a20d-6fcc21cf8bf7)

The proportion of non-diabetes patient in the dataset is 65%. We checked for multicollinearity in the dataset by performing a heat map plot to show the correlations among the features. This is displayed below:

![heat map](https://github.com/DannyRukks/Diabetes-Prediction-using-Machine-Learning-Classification/assets/97890440/4c4aaa03-a713-441d-bbee-988ea5a5c767)

# Classifier Models
The dataset was trained using logistic regression and three other classifiers such as KNearest neighbor classifier, Decision tree classifer and Random Forest classifier. All models used the same training and test splits and the same cross-validation method. The models were tune using hyper parameters and the best parameters were used for the prediction. The result for the models is displayed below
```
Results = pd.DataFrame({    
    "Methods" : ["Logistic Regression", "Decision Tree", "KNN", "Random Forest"],    
    "Train Accuracy" : [logreg_cv.best_score_, tree_cv.best_score_, knn_cv.best_score_, RF_cv.best_score_],
    "Test_Accuracy": METHOD   
})
Results
```
![Tabular result](https://github.com/DannyRukks/Diabetes-Prediction-using-Machine-Learning-Classification/assets/97890440/e87f6a14-4e4a-47f7-9b3b-4e62cc6a4876)

# Best Performing Model
Random forest seems to yield the best result when compared to other models in consideration. The model did better at predicting non diabetes patients but did fairly at predicting patients with diabetes. The confusion matrix of random forest model classifier is shown below.

![random forest](https://github.com/DannyRukks/Diabetes-Prediction-using-Machine-Learning-Classification/assets/97890440/a0dd128b-c8ae-4f40-bd77-c252b993559a)

# Key Findings and Insights
All the models except decision tree classifier performed well at predicting non diabetes patient. But the decision tree classifier performed well at predicting diabetes patients. Random Forest Classifier performs best. Random Forest Classifier had a training accuracy of 77.5% and test accuracy of 76.6%. 

# Recommendations
Based on the findings, it is highly recommended that there should be a balanced dataset for accurate predictions. Also, it is discovered that the more the number of rows of the dataset, the more likely that the accuracy of the result. I will also recommend the dataset should be tune with some other hyperparameters for the possibility of a better prediction.


