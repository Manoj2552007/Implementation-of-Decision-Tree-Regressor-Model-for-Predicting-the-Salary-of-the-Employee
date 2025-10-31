# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Collect dataset (employee details + salary).

2.Preprocess data (handle missing values, encode categorical features).

3.Split data into training and testing sets.

4.Initialize DecisionTreeRegressor with suitable hyperparameters.

5.Train the model on training data.

Predict salaries on test data.

6.Evaluate model performance (MAE, MSE, RMSE, R²).

7.Tune hyperparameters if needed.

8.Save and deploy the model for predictions.

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: Manoj R

RegisterNumber:  212224230152
```
import pandas as pd
import numpy as np
df=pd.read_csv("Salary.csv")
print(df.head())
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()
x=df[["Position","Level"]]
x.head()
y=df["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print("Reg no:212224230152")
print("name:Manoj R")
print(y_pred)
from sklearn.metrics import mean_squared_error,mean_absolute_error,r2_score
import numpy as np
mse=mean_squared_error(y_test,y_pred)
rmse=np.sqrt(mse)
mae=mean_absolute_error(y_test,y_pred)
r2=r2_score(y_test,y_pred)
print("Mean Squared Error:",mse)
print("Root Mean Squared Error:",rmse)
print("Mean Absolute Error:",mae)
print("R2 score:",r2)
dt.predict(pd.DataFrame([[5,6]],columns=["Position","Level"]))
```


## Output:
<img width="902" height="551" alt="image" src="https://github.com/user-attachments/assets/42189e9c-0006-4759-9422-bf61809dc5bd" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
