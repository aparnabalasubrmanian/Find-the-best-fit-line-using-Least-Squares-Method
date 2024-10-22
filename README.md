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
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: APARNA RB
RegisterNumber:  212222220005
*/
import numpy as np
import matplotlib.pyplot as plt
X= np.array(eval(input()))
Y= np.array(eval(input()))
X_mean= np.mean(X)
Y_mean= np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
b=Y_mean - m*X_mean
print(m,b)
Y_predicted=m*X + b
print(Y_predicted)
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='violet')
plt.show()
```

## Output:
# SLOPE AND Y-INTERCEPT:
![360801346-ec7cdb04-e2c5-4981-a98f-226160c3eb41](https://github.com/user-attachments/assets/fccfddd4-3ac3-40fa-9fd0-0d5bc86244f2)
# Y PREDICTED:
![360801442-589b2574-03d5-48e8-8459-acd8a5938197](https://github.com/user-attachments/assets/f10ea97f-0ee5-4a41-b977-acedd94793ff)
# GRAPH:
![365373501-3eed5b5b-242c-45b6-b105-9e661279a356](https://github.com/user-attachments/assets/9952c3eb-c0eb-4dac-a70c-55e3e1caa2dc)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
