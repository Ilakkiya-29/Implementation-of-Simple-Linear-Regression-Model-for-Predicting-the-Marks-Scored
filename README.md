# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Ilakkiya K
RegisterNumber: 212225040130
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Dataset: Study hours and marks scored
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 40, 50, 60, 65])

# Create the model
model = LinearRegression()

# Train the model
model.fit(X, Y)

# Predict marks
Y_pred = model.predict(X)

# Display results
print("Slope (m):", model.coef_[0])
print("Intercept (b):", model.intercept_)
print("Regression Equation: Y = {:.2f}X + {:.2f}".format(model.coef_[0], model.intercept_))

# Plotting
plt.scatter(X, Y, label="Actual Marks")
plt.plot(X, Y_pred, label="Predicted Line")
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.legend()
plt.show()
O
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
