## IMPLEMENTATION OF UNIVARIATE LINEAR REGRESSION
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
## Algorithm
```
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
4. Compute the y -intercept of the line by using the formula:
image
5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
Program:
```
## Program to implement univariate Linear Regression to fit a straight line using least squares.
```
/*

Developed by: SMRITI .B
RegisterNumber: 212221040156
*/
```
```

import numpy as np
import matplotlib.pyplot as plt
num_points=int(input("Enter the number of points"))
x = np.zeros(num_points)
y=np.zeros(num_points)
for i in range(num_points):
  x[i]=float(input(f"Enter x[{i}]: "))
  y[i]=float(input(f"Enter y[{i}]: "))


x_mean = np.mean(x)
y_mean = np.mean(y)


numerator = np.sum((x - x_mean) * (y - y_mean))
denominator = np.sum((x - x_mean)**2)
slope_m = numerator / denominator
intercept_b = y_mean - slope_m * x_mean


y_pred = slope_m * x + intercept_b


plt.scatter(x, y, label='Original Data')
plt.plot(x, y_pred, color='red', label='Regression Line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression')
plt.legend()
plt.show()

print(f"Slope (m): {slope_m}")
print(f"Intercept (b): {intercept_b}")
```
## Output:
![OUTPUT](https://github.com/smriti1910/UnivariateLinearRegression/assets/133334803/3bffbcab-c60c-4d3f-b986-29b9a2c3896c)

## RESULT:
  Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
