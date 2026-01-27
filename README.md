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
![WhatsApp Image 2026-01-27 at 9 34 12 AM](https://github.com/user-attachments/assets/523b50c1-6e55-4735-91bd-0c4d6ef70fda)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
