# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import the necessary libraries from python to execute the given code.
2. perform the logistic Regression on the given datasets.
3. perform the necessary opration to get the placement status whether placed or not placed.
4. print the predictive value of the model odf placement status.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: VESHWANTH.
RegisterNumber: 212224230300
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score,classification_report
data=pd.read_csv("C:\\Users\\admin\\OneDrive\\Attachments\\New folder (2)\\Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull()
data1.duplicated().sum()
le=LabelEncoder()
data1['gender']=le.fit_transform(data1['gender'])
data1['ssc_b']=le.fit_transform(data1['ssc_b'])
data1['hsc_b']=le.fit_transform(data1['hsc_b'])
data1['hsc_s']=le.fit_transform(data1['hsc_s'])
data1['degree_t']=le.fit_transform(data1['degree_t'])
data1['workex']=le.fit_transform(data1['workex'])
data1['specialisation']=le.fit_transform(data1['specialisation'])
data1['status']=le.fit_transform(data1['status'])
data1
x=data1.iloc[:,:-1]
x
y=data1['status']
y
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
lrt=LogisticRegression(solver="liblinear")
lrt.fit(x_train,y_train)
y_pred=lrt.predict(x_test)
y_pred
accuracy=accuracy_score(y_pred,y_test)
accuracy
classification_report1=classification_report(y_pred,y_test)
classification_report1
lrt.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:
![Screenshot 2025-03-19 094423](https://github.com/user-attachments/assets/b6889410-47fc-4597-9b26-824056cde9f3)
![5 2](https://github.com/user-attachments/assets/66434e91-3bba-4258-ad36-ee675da0e6c5)
![5 3](https://github.com/user-attachments/assets/1012a9a3-ad57-4b55-ae35-f9624bd56c90)
![5 4](https://github.com/user-attachments/assets/4b804567-097d-4265-b119-0c80d31f1e65)
![5 5](https://github.com/user-attachments/assets/cf89d744-7a52-40c4-ae27-3365c8166920)
![5 6](https://github.com/user-attachments/assets/ea090c27-3132-407b-844d-489d070f7cff)
![5 7](https://github.com/user-attachments/assets/609d424c-3dc3-4500-aa2e-f233cafc6e14)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
