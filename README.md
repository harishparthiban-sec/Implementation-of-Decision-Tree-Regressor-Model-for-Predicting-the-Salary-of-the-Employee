# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries: Pandas, Matplotlib, and DecisionTreeRegressor from scikit-learn.
2.Load the dataset and separate input features X and target variable Y (Salary).
3.Convert categorical features into numeric values using dummy variables.
4.Split the dataset into training and testing sets.
5.Create and train the Decision Tree Regressor model using the training data.
6.Plot and display the decision tree structure with feature names. 

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Harish P
RegisterNumber:  212225040115
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
data = pd.read_csv("Salary (1).csv")
x = data.drop("Salary", axis=1)
y = data["Salary"]
x = pd.get_dummies(x, drop_first=True)
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(x_train, y_train)
plt.figure(figsize=(25,12))
plot_tree(model,feature_names=x.columns,filled=True)
plt.title("Decision Tree Regressor")
plt.show()
```

## Output:
<img width="1338" height="652" alt="image" src="https://github.com/user-attachments/assets/0ad0e0ba-36a2-4abf-b569-cc907203badc" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
