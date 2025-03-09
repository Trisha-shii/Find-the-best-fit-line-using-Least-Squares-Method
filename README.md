# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Trisha Priyadarshni Parida
RegisterNumber: 212224230293
*/

```import numpy as np
import matplotlib.pyplot as plt

#input values of independent variable X & dependent variable Y

X = np.array([10,20,30,40,50])
Y = np.array([15,23,38,46,59])

#means, x bar and y bar

X_Mean = np.mean(X)
Y_Mean = np.mean(Y)

#y = mx+c, m = num/den, num = summation of (x-Mean_X)*(y-Mean_Y), den = summation of (x-mean_X)^2, c = y - mx, y = Y_Mean & x = X_Mean

#Slope m

num = np.sum((X-X_Mean)*(Y-Y_Mean))
den = np.sum((X-X_Mean)**2)
m = num/den

#y-intercept c

c = Y_Mean -(m*X_Mean)

#Equation of the line format => 'y' = m'x'+c, Display eqn of linear regression

print(f"Equation of the line: Y = {m:.2f}X + {c:.2f}")  #  {co-efficients of x, i.e, m & constant c}

#plotting the graph with linear regression line/best fit line in red and data points/values in blue

plt.scatter(X,Y,color = "red", label = "Data Points")   #Scatter Plot

#Create list of dependent variable Y's_Expected values acc to eqn of line,

Y_Predicted = (m*X) + c

plt.plot(X,Y_Predicted,color = "blue", label = "Best Fit Line")      #Line Plot Default 

plt.title("UNIVARIATE LINEAR REGRESSION")
plt.xlabel("INDEPENDENT VARIABLE")
plt.ylabel("DEPENDENT VARIABLE")
plt.legend()
plt.show()
```

## Output:

![Screenshot 2025-03-09 201341](https://github.com/user-attachments/assets/90e019bb-9759-40c2-92cd-e4226b475d15)

![Screenshot 2025-03-09 201347](https://github.com/user-attachments/assets/f674fab8-a414-4ec0-94d6-da857c660b25)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
