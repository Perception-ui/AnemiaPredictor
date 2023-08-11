# Anemia Detection and Severity Classification in Kenya: A Predictive Statistics

## Business Understanding

### Introduction

The **Kenya Medical Research Institute (KEMRI)** is a vital institution in Kenya's healthcare landscape. Established in 1979, it operates as the national body responsible for conducting research in human health, providing advice to the Ministry of Health (MOH), and contributing to healthcare and delivery improvement. KEMRI's mission includes research, capacity building, innovation, and service delivery to enhance human health and quality of life. This project focuses on addressing the challenge of anemia, a condition affecting various populations and posing a significant public health concern.

### Problem Statement

Efficient and accurate detection of anemia and its severity is crucial for effective healthcare management. The current diagnostic tools lack precision, leading to delayed interventions, poor outcomes, and increased healthcare costs. KEMRI, commissioned by the MOH, aims to develop predictive models using comprehensive blood count parameters, age, and gender to enhance anemia detection's efficiency and accuracy. This project seeks to provide data-driven insights that will improve patient care, decision-making, and healthcare policies.

### Defining Metrics of Success

The success of the predictive model will be evaluated based on its ability to provide accurate predictions of anemia levels concerning age, gender, and comprehensive blood count parameters.

### Research Questions

- What are the key predictors of anemia levels?
- How does gender impact the risk of anemia?
- How does age influence the risk of anemia?
- What is the relationship between blood parameters and hemoglobin levels?
- How well does the selected model generalize to new data?

### Main Objective

The main objective of this project is to develop a predictive model using comprehensive blood count parameters, age, and gender to facilitate early and accurate detection of anemia presence and severity.

### Specific Objectives

- Investigate the most important predictors of anemia levels.
- Explore the relationship between age and the risk of anemia.
- Analyze how age affects the risk of anemia.
- Examine the relationship between hemoglobin levels and various comprehensive blood count parameters.
- Develop a predictive model capable of accurately predicting anemia levels based on age, gender, and other blood count parameters.

## Data Understanding

The dataset used in this project consists of comprehensive blood count (CBC) test results obtained from a Hematology analyzer. It contains 11 attributes for each patient, including age, gender, and various CBC parameters such as hemoglobin level, mean cell volume, mean cell hemoglobin, red cell distribution width, white blood cell count, platelet count, and more.

- Age: Numerical attribute representing the age of patients (11 to 100 years).
- Gender: Categorical attribute representing the gender of patients (Male or Female).
- Hemoglobin (HGB): Numerical attribute indicating hemoglobin level in blood.
- Mean Cell Volume (MCV): Numerical attribute indicating the mean volume of a red blood cell.
- Mean Cell Hemoglobin (MCH): Numerical attribute indicating the mean amount of hemoglobin in a red blood cell.
- Red Cell Distribution Width (RDW): Numerical attribute indicating the variation in red blood cell size.
- White Blood Cell Count (WBC): Numerical attribute indicating the count of white blood cells.
- Platelet Count (PLT): Numerical attribute indicating the count of platelets.
- Packed Cell Volume (PCV): Numerical attribute indicating the volume percentage of red blood cells.
- And more.

## Importing Necessary Libraries

The required Python libraries are imported to perform data analysis, visualization, preprocessing, and building predictive models. The libraries include pandas, numpy, matplotlib, seaborn, scikit-learn modules, and more.

## Reading into the Data

The dataset is loaded using pandas, and the first few rows are displayed to get a glimpse of the data's structure.

#### Data Wrangling
Before applying machine learning models, the dataset underwent a thorough data wrangling process to ensure its quality and compatibility. This process included steps such as:

- **Handling Missing Values:** Any missing values in the dataset were identified and handled appropriately. This might involve imputation techniques or, in some cases, removing rows or columns with significant missing data.

- **Data Transformation:** Data was transformed to make it suitable for analysis. This could include converting categorical variables to numerical representations (like one-hot encoding) and normalizing or standardizing numerical features.

#### Data Cleaning
During the data cleaning phase, various techniques were applied to ensure the dataset's integrity and consistency:

- **Removing Duplicate Entries:** Duplicate rows or records, if any, were removed to avoid skewing the analysis or modeling process.

- **Outlier Handling:** Outliers, which could affect the model's performance, were identified and addressed using appropriate methods like trimming or transformation.

- **Correcting Inconsistent Data:** Any data inconsistencies, like conflicting values or wrong entries, were identified and corrected.

- **Ensuring Data Quality:** The dataset was reviewed for data quality issues such as typos, inconsistent formats, or data entry errors, and these were rectified.

## Modeling

### First Model - K-Nearest Neighbors

K-Nearest Neighbors (KNN) is implemented as the first predictive model. The data is split into training and test sets, scaled using StandardScaler, and OneHotEncoder is used for encoding target variables. The KNeighborsClassifier is trained and evaluated using accuracy and F1-score metrics.

### Second Model - Decision Tree Classification

A Decision Tree classifier is implemented as the second model. The classifier is trained on the training data, and accuracy, F1-score, and confusion matrix are calculated.

### Third Model - Support Vector Machines (SVM)

The third model utilizes Support Vector Machines (SVM) for classification. The dataset is split, scaled using MinMaxScaler, and SVM is trained. Accuracy and F1-score are calculated for evaluation.

### Fourth Model - Gradient Boosted Decision Trees

The fourth model employs Gradient Boosted Decision Trees. Accuracy, F1-score, and a confusion matrix are computed to assess the model's performance.

### Fifth Model - Ensembling with Random Forests

A Random Forests classifier is implemented as the fifth model. Accuracy, F1-score, and a confusion matrix are calculated to evaluate the model.

### Model Tuning and Hyperparameter Optimization

GridSearchCV is utilized to tune the hyperparameters of the models. The best parameters for Decision Trees and Gradient Boost
### Conclusions
Blood Parameters like haemoglobin, Packed Cell Volume and Red Blood Cell counts appears to be the primary predictors of Anemia Levels in patients.

Sex appears to be a factor in the prevalence of different levels of Anemia in patients. Mild Anemia is more prevalent in females than males.Moderate/Severe Anemia is more prevalent in males than females.

Age also appears to be a factor in the prevalence of Anemia.People in the range of 40-49 and 70-79 years appears to be more prevalent to moderate/severe anemia and people of age ranges 20-29 and 50-59 years are more prevalent to mild anemia.

The model selected random forest model with an accuracy

### Recommendations
Features like haemoglobin, packed cell volume and red blood cell count should be the primary predictors when detecting anemia levels in patients.

Specific age groups like 40-49 and 70-79 years should submit to regular screening because they are more suseptible to moderate/severa anemia.

Further data should be collected on more people on the various blood parameters to increase the size of data used to train the model leading to a better performing model.

Further research should be done to investigate the relationship between acohol consumption and moderate/severe anemia.
