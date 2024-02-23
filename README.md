# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard Libraries. 
2.Set variables for assigning dataset values.
3.Import linear regression from sklearn. 
4.Assign the points for representing in the graph. 
5.Predict the regression for marks by using the representation of the graph. 
6.Compare the graphs and hence we obtained the linear regression for the given datas.
## Program:

/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: GANESH S
RegisterNumber: 212222040042
*/
```
import numpy as np
import matplotlib.pyplot as plt

# proceeding input data
X = np.array(eval(input()))
Y = np.array(eval(input()))

# mean
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0 #for slope
denom=0 #for slope

# to find sum of(xi-x')&(yi-y')&(xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean*(Y[i]-Y_mean))
    denom+=(X[i]-X_mean)**2

#calculate slope
m=num/denom

# calculate intercept
b=Y_mean-m*X_mean

print(m,b)

# line equation
Y_predicted=m*X+b
print(Y_predicted)

# to plot graph
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='red')
plt.show()
```
## Output:

![ml ex 1](https://github.com/ganeshshanmugavel27/Find-the-best-fit-line-using-Least-Squares-Method/assets/122046208/30dc9723-e623-4da1-9031-70d9fa52019c)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
