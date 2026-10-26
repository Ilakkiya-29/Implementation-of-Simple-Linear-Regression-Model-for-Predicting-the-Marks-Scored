# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries such as NumPy, Matplotlib, and scikit-learn.
2. Enter the dataset containing study hours (independent variable) and marks scored (dependent variable).
3. Reshape the independent variable into the required format.
4. Create the simple linear regression model.
5. Train the model using the given data.
6. Predict the marks using the trained model.
7. Display the regression equation and plot the regression line. 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Ilakkiya K
RegisterNumber: 212225040130
*/
import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error, mean_squared_error
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
df = pd.read_csv('exp_2_dataset_student_scores.csv')
print("First 5 rows:\n", df.head(), "\n")
print("Last 5 rows:\n", df.tail(), "\n")
X = df.iloc[:, :-1].values
Y = df.iloc[:, -1].values
print("X (features):", X.flatten())
print("Y (targets):", Y)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size=1/3, random_state=0)
print("\nTraining samples:", len(X_train), " Testing samples:", len(X_test))
regressor = LinearRegression()
regressor.fit(X_train, Y_train)
Y_pred = regressor.predict(X_test)
print("\nPredicted values:", np.round(Y_pred, 2))
print("Actual values   :", Y_test)
plt.figure(figsize=(6,4))
plt.scatter(X_train, Y_train, color="orange", label="Training data")
plt.plot(X_train, regressor.predict(X_train), color="red", label="Fitted line")
plt.title("Hours vs Scores (Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.legend()
plt.grid(True)
plt.show()
```

## Output:
<img width="661" height="478" alt="image" src="https://github.com/user-attachments/assets/d0bab55b-1b90-448a-ab9f-273941b8b96d" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
