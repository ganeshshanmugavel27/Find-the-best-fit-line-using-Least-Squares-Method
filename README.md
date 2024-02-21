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
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: GANESH S
RegisterNumber: 212222040042
*/

import pandas as pd
df=pd.read_csv('/content/TABLE 1 - Sheet1.csv')
df
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv('/content/TABLE 1 - Sheet1.csv')
df.head(10)
plt.scatter(df['x'],df['y'])
plt.xlabel('x')
plt.xlabel('y')
x=df.iloc[:,0:1]
y=df.iloc[:,-1]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LinearRegression
lr=LinearRegression()
lr.fit(x_train,y_train)
x_train
y_train
lr.predict(x_test.iloc[0].values.reshape(1,1))
plt.scatter(df['x'],df['y'])
plt.xlabel('x')
plt.xlabel('y')
plt.plot(x_train,lr.predict(x_train),color='red')
```

## Output:
![image](https://github.com/ganeshshanmugavel27/Find-the-best-fit-line-using-Least-Squares-Method/assets/122046208/24ca6c21-e9fc-4e5b-8a82-7c03c924e953)
![image](https://github.com/ganeshshanmugavel27/Find-the-best-fit-line-using-Least-Squares-Method/assets/122046208/4667effc-1141-4abf-8562-601568826e5e)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
