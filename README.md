# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:SUBIKSHA K
RegisterNumber: 212224040332

```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```

```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
R2 score:  0.48611111111111116

```
```
dt.predict([[5,6]])
```

## Output:

<img width="958" height="299" alt="390836269-a61bc2cc-84ea-456b-b431-6814e70f21e9" src="https://github.com/user-attachments/assets/c4c78a56-97cd-4dc1-9fdd-3c16ef6a8e06" />

<img width="399" height="195" alt="390836348-b85ac197-8498-48ee-b61a-e1bfb45397ee" src="https://github.com/user-attachments/assets/a9e2c2fe-8506-4582-ac8d-867c1fd6d94d" />

<img width="697" height="131" alt="390836414-eb0865da-4ded-400b-a133-5bd3868eb59c" src="https://github.com/user-attachments/assets/a7d59eb4-87c2-4177-a0b2-ae47e6f715b3" />

<img width="323" height="35" alt="390836467-f2538dc7-b3d6-4927-9403-1ba953b50548" src="https://github.com/user-attachments/assets/229871ee-295f-49fd-9eda-4731753679d0" />


<img width="200" height="35" alt="390836522-6b53be8b-b5c2-4b09-a220-1ec50aea4747" src="https://github.com/user-attachments/assets/def11df9-ae3e-4fef-a8b0-8978862a0b62" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
