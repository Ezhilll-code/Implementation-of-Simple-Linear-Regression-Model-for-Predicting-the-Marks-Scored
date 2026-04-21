# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import Required Libraries
Import numpy, matplotlib.pyplot, and LinearRegression from sklearn.linear_model.
2. Initialize Dataset
Define the independent variable X (hours studied) and dependent variable Y (marks scored).
Reshape X into a 2D array as required by sklearn.
3. Define the Model
Create an object of the Linear Regression model:

model = LinearRegression().

4. Fit the Model (Training Phase)
Train the model using:

model.fit(X, Y)

The model internally computes the best-fit line using the equation:
<img width="235" height="64" alt="image" src="https://github.com/user-attachments/assets/40a87e22-a5cd-412c-9c37-164ba1eba495" />
where:
m = coefficient (model.coef_)
b = intercept (model.intercept_).

5. Extract Model Parameters
Obtain:

Slope: m=model.coef_
Intercept: b=model.intercept_.

6. Prediction Step
For a new input x, predict marks using:

y=mx+b

Implemented as:

model.predict([[x_input]]).

7. Generate Predicted Values for Visualization
Compute predicted outputs for all X:

Y_pred = model.predict(X).

8. Plot the Graph

Plot actual data using scatter plot
Plot regression line using predicted values.

9. Display Output
Print slope, intercept, and predicted marks.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Ezhilan H
RegisterNumber: 212225240040

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([33, 55, 66, 77, 88])

model = LinearRegression()

model.fit(X, Y)

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
*/
```

## Output:

<img width="922" height="690" alt="image" src="https://github.com/user-attachments/assets/0bf1c76e-e6cb-4563-a709-6317806e5b05" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
