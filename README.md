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
## Program
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: N.Kishore
Register number: 212222240049

import numpy as np
import matplotlib.pyplot as py
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num,den=0,0
for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  den+=(x[i]-x_mean)**2
m=num/den
b=y_mean-(m*x_mean)
print(m,b)
y_pred=(m*x)+b
print(y_pred)
py.scatter(x,y,color="blue")
py.plot(x,y_pred,color="red")
py.show()

```
## Output

![Screenshot 2023-06-09 213848](https://github.com/nkishore2210/Univariate-Linear-Regression/assets/118707090/b710a398-8f7c-45f8-802f-e0c874ae3390)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
