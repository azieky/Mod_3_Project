## Heart Disease Project

## Introduction

It is anticipated that the development of computation methods that can predict the presence of heart disease will significantly reduce heart disease caused mortalities while early detection could lead to substantial reduction in health care costs.

Heart disease is currently the leading cause of death across the globe. Prediction of cardiovascular disease is regarded as one of the most important subjects in the section of clinical data analysis. This makes heart disease a major concern to be dealt with. But it is difficult to identify heart disease because of several contributory risk factors such as diabetes, high blood pressure, high cholesterol, abnormal pulse rate, and many other factors. Due to such constraints, scientists have turned towards modern approaches like Machine Learning for predicting the disease.

This dataset contains some medical information of patients which tells whether that person getting a heart attack chance is less or more. Using the information, we want to explore the dataset and classify the target variable and use different Machine Learning models and find out which model and metric is best suitable for this dataset, and lastly if the dataset useful for future heart disease predictions.  

#### Also, in this project, we will go through the dataset to see: 

1. Which age group had most heart disease?
2. Is male more likely to have heart disease than female?
3. What are the top features?

#### The project consists of 5 phases:

•	Phase 1 Importing the Dataset

•	Phase 2 EDA

•	Phase 3 Feature Engineering

•	Phase 4 Feature Selection

•	Phase 5 Modeling 

#### Libraries Used

•	Panda

•	Numpy

•	Math

•	Matplotlib.pyplot

•	Random

•	Seaborn

•	Math

•	Re

•	Sklearn

•	Statsmodels

## DataSet

The objective of this project is to build a model to predict whether a person diagnose a heart disease based on pattern extracted from analyzing 13 descriptive features plus 1 target column and 1025 observation found in Cleveland, Hungary, Switzerland, and Long Beach V data set from Kaggle website. The "target" column refers to the presence of heart disease in the patient. It is integer valued 0 = no disease and 1 = disease.

### The remaining 13 features are described in the section below.

1.	age: age 
2.	sex: sex (1 = male; 0 = female)
3.	cp: chest pain type (4 values). Categorical with 4 levels: Type 1: Typical angina. 
Type 2: Atypical angina. Type 3: Non-anginal pain. Type 4: Asymptomatic
4.	trestbps: resting blood pressure 
5.	chol: serum cholesterol in mg/dl 
6.	fbs: fasting blood sugar > 120 mg/dl 
7.	restecg: resting electrocardiographic results (values 0,1,2) 
8.	thalach: maximum heart rate achieved 
9.	exang: exercise induced angina
10.	oldpeak: ST depression induced by exercise relative to rest 
11.	slope: the slope of the peak exercise ST segment 
12.	ca: Number of major vessels (0–4) colored by fluoroscopy
13.	thal: 0 = normal; 1 = fixed defect; 2 = reversable defect

## Data Cleaning

No major issue with our data. Our dataset didn’t have any null or nan values. The only major issue we had was understanding the feature columns and renaming it

## Analysis

   After formatting our data into a useable state, we used various categorization and statistical analysis methods to find answers to our business questions. We took different machine learning algorithm and tried to find algorithm which predict accurately. We used K-Nearest Neighbor, Logistic Regression, Random Forest Classifier, and Decision Tree Classifier. Also, for our metric classification we chose Recall. The reason we chose Recall was because we don’t want to accidentally discharge a heart disease patient. Also, we wanted to classify the maximum number of patients who end up having a cardiac disease with the positive class. After we ran several models, Decision Tree Classifier had the highest score in our model testing.

#### 1. Which age group had the highest heart disease?

We grouped our age column into three groups. Since the dataset patients age started from 29, the first group (Young) were between 29 to 40, our second group (Mid-Age) were between 40 to 55, and our third group (Above) were 55 and up. After working and graphing the data Interestingly, we saw patients that were Mid-Age had the highest heart disease followed by above 55. This can be an indicator that heart disease starting point can be in mid age an up, so people over 40 have to be regularly checked for so any heart disease can be prevented. 

#### 2. Is male more likely to have heart disease than female?

Our data shows that males are more likely to get heart disease than females. We have to mention that we had more male patients in our dataset than female, and from these patients 413 at of 713 male patients had heart disease and 226 at of 312 female patients had heart disease. We can see by this observation males are more likely to visit the hospital or clinic with heart disease symptom than female. 


#### 3. What are the top features?

Based on our analyzation Chest Pain, Major Vessels, and Thalassemia were our top features in heart disease. 

#### Chest Pain: 
There were 4 categorize of chest pain in our dataset.  
Type 1: Typical angina. Type 2: Atypical angina. Type 3: Non-anginal pain. Type 4: Asymptomatic. We saw most patients who had non-anginal type of chest pain had the highest ratio heart disease followed by atypical angina, and asymptomatic. Patients with typical angina had the lowest heart disease ratio, and at the same time approximately 497 of patients of the dataset have typical angina. From those only about 120 have heart disease. 

#### Max Heart Rate: 
Which is number of major vessels (0–4) colored by fluoroscopy. Fluoroscopy is used to help the healthcare provider see the flow of blood through the coronary arteries to check for arterial blockages. Based on evaluation patients who fall in 0 category have highest heart disease ratio, followed 4 category which was the lowest number of patients but high ratio. Category 3 had least number of patents who had heart disease. Category 1 and 2 were almost the same in terms of ratio, but also had high number of heart disease patients followed category 0.

#### Thalassemia: 
Is a blood disorder passed down through families (inherited) in which the body makes an abnormal form or inadequate amount of hemoglobin. Hemoglobin is the protein in red blood cells that carries oxygen. The disorder results in large numbers of red blood cells being destroyed, which leads to anemia. Our finding showed most patients fall on either category 2 or 3. Category 2 had largest number of patients and most patients who were in this category had heart diseases compare to other categories. Category 3 had largest number of patients who did not have heart disease. The fewest patient category was 0, only 7 patients were in this category. 

   After analyzing the data and getting unusual high scores in our models, which is good to have high scores, but at the same time we want to make sure our model is not biased or doesn’t have duplicated data, so because of that we did further investigation to rule out those assumptions. After we investigated, we found out there were 723 duplications in the dataset.  Unfortunately, because of that we had to eliminate those data to make sure our dataset is clean and unbiased for prediction. At this stage, we feel more comfortable if we can get more patients data sample to make sure our model is accurate in predicting heart disease.    

## Conclusion

Heart Disease is one of the major concerns for society today. It is difficult to manually determine the odds of getting heart disease based on risk factors. However, machine learning techniques are useful to predict the output from existing data. 

Based on analysis we found mid aged males are vulnerable to heart diseases than females. Also, Chest Pain, Major Vessels, and Thalassemia were the top features of this data. We recommend that both male and female above 40 do regular checking for heart disease so it can preventable at early stages. 

Due to unusual very high scores in our models we had investigate and eliminate 723 observations due to high multiple duplications. will would like to investigate further to make sure our model is not biased, and our dataset doesn’t have duplicates inputs.

### Further Analysis:

#### To continue this project, we would suggest:

•	Augmenting the dataset with additional sources

•	Re-collecting data as more becomes available

•	Automating collection and analysis methods to always have up to date information


