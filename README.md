# Implementation of Univariate Linear Regression

## Aim:

To implement univariate Linear Regression to fit a straight line using least squares.

## Equipment’s required:

1.	Hardware – PCs

2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

1.	Get the independent variable X and dependent variable Y.

2.	Calculate the mean of the X -values and the mean of the Y -values.

3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)

4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  

5.	Use the slope m and the y -intercept to form the equation of the line.

6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
# Univariate Linear Regression
# Developed by: Amruthavarshini Gopal
# Register number: 23000851

import numpy as np
import matplotlib.pyplot as plt
x= np.array(eval(input()))
y=np.array(eval(input()))
X=np.mean(x)
Y=np.mean(y)
num,den=0,0
for i in range (len(x)):
  num +=((x[i]-X)*(y[i]-Y))
  den += ((x[i]-X)**2)
m=num/den
b=Y-m*X
print(m,b)
Ypred = m*x + b
print(Ypred)

plt.scatter(x,y)
plt.plot(x,Ypred,color='red')
plt.show()

```
## Output:
![Alt text](uni.png)

## Result:

Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
