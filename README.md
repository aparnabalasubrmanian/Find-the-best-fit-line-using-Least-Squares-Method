# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1: Start

STEP 2: Get the independent variable X and dependent variable Y.

STEP 3: Calculate the mean of the X -values and the mean of the Y -values.

STEP 4: Find the slope m of the line of best fit using the formula. 


<img width="231" alt="ml i" src="https://github.com/user-attachments/assets/cb45e0fb-01be-41f6-aa28-fa7ca704485a">

STEP 5: Compute the y -intercept of the line by using the formula:

<img width="148" alt="mlj" src="https://github.com/user-attachments/assets/c6abc8f7-50bc-45e8-9dad-4b689654f6b6">


STEP 6: Use the slope m and the y -intercept to form the equation of the line.

STEP 7:  Obtain the straight line equation Y=mX+b and plot the scatterplot.

STEP 8: End

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: APARNA RB
RegisterNumber:  212222220005
*/

import numpy as np
import matplotlib.pyplot as plt

#preprocessing input data

X=np.array(eval(input()))
Y=np.array(eval(input()))


#mean

X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0 #for slope
denom=0 #for slope


#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2


#to find slope

m=num/denom
b=Y_mean-m*X_mean
print(m,b)

#to find predicted value
 
Y_predicted=m*X+b
print(Y_predicted)


#to plot graphplt.scatter(X,Y)

plt.plot(X,Y_predicted,color="red")
plt.show()

```

## Output:
# SLOPE AND Y-INTERCEPT:
![Screenshot 2024-08-23 105446](https://github.com/user-attachments/assets/ec7cdb04-e2c5-4981-a98f-226160c3eb41)

# Y PREDICTED:
![Screenshot 2024-08-23 105452](https://github.com/user-attachments/assets/589b2574-03d5-48e8-8459-acd8a5938197)

# GRAPH:
![Screenshot 2024-08-23 105459](https://github.com/user-attachments/assets/bc7bd28d-0caa-41c7-816a-6198d90317c9)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
