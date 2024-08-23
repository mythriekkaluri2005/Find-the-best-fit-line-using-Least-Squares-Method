# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

STEP-1: Start

STEP-2: Get the independent variable X and dependent variable Y.

STEP-3: Calculate the mean of the X -values and the mean of the Y -values.

STEP-4: Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

STEP-5: Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

STEP-6: Use the slope m and the y -intercept to form the equation of the line.

STEP-7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

STEP-8:End.








## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: E.Mythri
RegisterNumber:  212223240034
*/

import numpy as np
import matplotlib.pyplot as plt

#preprocessing input data

X=np.array(eval(input()))
Y=np.array(eval(input()))
#Mean
X_mean = np.mean(X)
Y_mean = np.mean(Y)
num=0
denom=0
#to find sum of (xi-x') &(yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i] -X_mean)*(Y[i]-Y_mean)
    denom+= (X[i]-X_mean)**2
# calculate slope
m=num/denom

#calculate intercept
b=Y_mean-m*X_mean
print(m,b)
#line equation
y_predicted=m*X+b
print(y_predicted)
#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()

```

## Output:
## slope and y-intercept
6.49131274131274 33.76833976833977

## Y predicted
![Screenshot 2024-08-23 105324](https://github.com/user-attachments/assets/cfe0d981-979e-446d-a4c7-23ef3fa30af6)

## Graph
![Screenshot 2024-08-23 105353](https://github.com/user-attachments/assets/12c9fa25-d95b-4a1e-aac2-d03356d01886)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
