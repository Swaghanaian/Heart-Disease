# Heart-Disease

##Analysis of 12 medical attributes gathered to predict the occurence of heart disease

###Overview
This project highlighted 12 medical attributes related to heart disease in order to predict whether a patient has existing Heart disease or not. The project is broken down into 3 parts. Part 1 entails Inspecting the data and cleaning the data where necessary for missing values or inconsistent values. Part 2 looked at Data visualization, where some of the features were ploted on graphs to view their relationship with Heart Disease. Part 3 involved using 3 classification machine learning models to determine which models provided the best predictions for the occurence of Heart disease. The PCA feature engineering technique was applied to the models to assess if there improve the model results or made the predictions worse. 


####Dataset

Data Source
https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction?resource=download

![image](https://user-images.githubusercontent.com/103012497/186909051-55ee01c3-4937-4654-b7dd-e8ac9c54d402.png)

The data contains 12 columns and 918 rows. 5 of the features are numeric data(Age, Resting Blood Pressure, Cholesterol, Max Heart Rate and Old Peak) and 7 of the features are categorical data(Sex, Chest Pain Type, FastingBS, Resting ECG, Exercise Angina and ST_Slope). The data also had 725 of the patient sample representing the male sex.

![image](https://user-images.githubusercontent.com/103012497/186911796-c67b2242-f222-47da-99d4-f8638b28177c.png)

#####Process
The cholesterol columnm had a minimum value of 0. High Cholesterol increases a patients risks for HeartDisease and Lower Cholesterol levels are generally good but 0 level could be an indicator that the value was missing and replaced with 0. I used my judgment to replace that value with the mode value of the dataset which still returned 0 as 0 was the most frequent value. I finally decided to used the mean which returned a value of 85.


######Analysis

![image](https://user-images.githubusercontent.com/103012497/186914712-472a3161-7ed7-44b3-9f88-575b94f4c313.png)

The graph above is showing the distribution of the oldpeak feature relative to heart disease. The oldpeak features refers to the ST depression induced by exercise relative to rest. This is the stress caused by the amount of effort exerted in exercise or physical activity. The results from the dataset shows a positive correlation between this feature and Heart Disease. Patients with higher level of oldpeak(around 1.2) can be advised to reduce the amount of effort exerted in exercise or physical activity they are currently partaking in to reduce the risk of getting Heart Disease.


![image](https://user-images.githubusercontent.com/103012497/186916068-830f7112-43cd-44c3-b3fa-b2f6e12d21ec.png)

The graph above shows the percentage of Male and Female with Heart Disease. From the dataset provided, about 64% of the Male instances have Heart Disease and 26% of the Female instances have Heart Disease. Maybe Male patients should be advised to schedule appointments regularly to assess their risk for Heart Disease. Note: There were more male samples(725) in the dataset(918)


![image](https://user-images.githubusercontent.com/103012497/186916488-6a76ca5f-7360-4dca-80b6-10dc45c422fe.png)

The Age distribution above shows that the risk of Heart Disease increases as patients age. To reduce these risks Patients 45 and older can be advised to adopt healthier lifestyles like eating healthy, getting regular exercise and being on a lower fat diet to reduce the risk of getting Heart Disease.



#######Final Model

False negatives are the most important metrics to consider with this project. This is because results showing that a patient is negative for HeartDisease when they are actually positive can be problematic. This can cause patients with HeartDisease to have a delay in treatment which can put their lives at risk. With that being said, the best model with the best results in predicting false negatives is the final random forest model which has a false negative prediction of 9%. This model may be useful in production but I think 9% is still a high percentage of false negatives and is material to the quality of results you want to provide to patients as it can be life threatening.


########Recommendations
The concern raised about the final model's prediction can however, be reduced by adding more data to train the model to possibly get the prediction results lower than 5% or. Adding some more features or removing some of the attributes after talking to a subject matter expert is also another recommendation.

#########Contact
Name: David Addo
Email: [addodavid4410@gmail.com](url)
