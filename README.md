# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries and load the dataset from the CSV file
2. Separate the dataset into independent variable (Experience) and dependent variable (Salary).
3. Create the Linear Regression model and train it using the given data.
4. Predict the salary values, display slope and intercept, and plot the regression line with the data points. 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Shankar S B
RegisterNumber:  212225230260
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()


model.fit(X, Y)

# Get slope and intercept
m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)


x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])


Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

```

## Output:
<img width="774" height="648" alt="Screenshot 2026-04-21 112649" src="https://github.com/user-attachments/assets/1dd1eedc-71f0-4dd6-97aa-7a163c8edcdf" />




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
