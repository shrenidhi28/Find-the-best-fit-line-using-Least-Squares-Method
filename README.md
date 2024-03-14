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
Developed by: C.SHRENIDHI
RegisterNumber:  212223040196
*/
```
import numpy as np <br>
import matplotlib.pyplot as plt <br>
x=np.array(eval(input())) <br>
y=np.array(eval(input())) <br>
x_mean=np.mean(x) <br>
y_mean=np.mean(y) <br>
c=0 <br>
e=0<br>
for i in range(len(x)):<br>
a=x[i]-x_mean<br>
b=y[i]-y_mean<br>
c=c+a*b #sum of (x-xmean)*(Y-ymean)<br>
d=a*a<br>
e=e+d #sum of (x-xmean)^2<br>
m=c/e<br>
#y intercept or c in line equation<br>
n=(y_mean)-(m)*(x_mean)<br>
print(m,n)<br>
y_predicted=m*x+n<br>
print(y_predicted)<br>
plt.scatter(x,y)<br>
plt.plot(x,y_predicted,color="red")<br>
plt.show()<br>
[3.6,4.8,7.2,6.9,10.7,6.1,7.9,9.5,5.4]<br>
[9.3,10.2,11.5,12,18.6,13.2,10.8,22.7,12.7]<br>
1.537302371541502 2.8370580808080827<br>
[ 8.37134662 10.21610946 13.90563516 13.44444444 19.28619346<br>
12.21460255<br>
14.98174682 17.44143061 11.13849089]<br>

## Output:
<img width="408" alt="image" src="https://github.com/AkilaMohan/Find-the-best-fit-line-using-Least-Squares-Method/assets/155261096/84c08faf-f209-4241-92d1-768f1fcfbc8e">



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
