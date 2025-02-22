# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Load the Salary.csv dataset, display the initial rows (head), and examine the data structure (info) to check for missing values.

2.Encode the "Position" column using LabelEncoder to convert it into numeric format, making it suitable for regression modeling.

3. Define the feature set x (including "Position" and "Level") and target y ("Salary"), and split these into training and testing sets with an 80-20 ratio using train_test_split.

4. Train a DecisionTreeRegressor on the training data to model the relationship between features and salary.

5. Evaluate the model's performance using the Mean Squared Error and R² score, and make predictions for new sample inputs, e.g., dt.predict([[5,6]]).
   
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: PRIYADHARSHINI S
RegisterNumber: 212223240129

import pandas as pd
data=pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position", "Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train, y_test=train_test_split(x, y, test_size=0.2, random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
*/
```

## Output:
![Screenshot 2024-10-29 135211](https://github.com/user-attachments/assets/4eb89322-5372-4b72-a34e-179aea7dda14)

## MSE:
![Screenshot 2024-10-29 135256](https://github.com/user-attachments/assets/fc016a96-17a3-433a-9c70-70185849b281)

## R2:
![Screenshot 2024-10-29 135341](https://github.com/user-attachments/assets/2b661047-5a8d-4dbc-a683-2c028e3ec59f)

## Predicted:
![Screenshot 2024-10-29 135347](https://github.com/user-attachments/assets/994d2d3b-9181-4a9d-af0c-1cecefa875f2)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
