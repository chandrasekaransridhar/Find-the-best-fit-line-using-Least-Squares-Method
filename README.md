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
~~~py
#univarite simple linear regression
#univarite simple linear regression
import numpy as np
import matplotlib.pyplot as plt
x=np.array([1,2,3,4,5])
y=np.array([20,40,60,80,100])
if(len(x)!=len(y)):
    raise SystemExit("the len x and y is not same")
    
no_of_observations=len(x)

X_mean=np.sum(x)/no_of_observations

Y_mean=np.sum(y)/no_of_observations

numerator=np.sum((x-X_mean)*(y-Y_mean))

denominator=np.sum((x-X_mean)**2)

m=numerator/denominator

c=Y_mean-m*X_mean
Y_predict=m * x + c

print(f"slope of the line (m) = {m}")
print(f"intercept (c) = {c}")
print(f"predicted output = {Y_predict}")
plt.scatter(x,y,color="blue",label="actual data")
plt.grid()
plt.plot(x,Y_predict,color="green",label="Predicted data")
plt.xlabel("Student hours",color="Red",fontsize=16)
plt.ylabel("Marks",color="blue",fontstyle="italic",fontsize=16)
plt.title("Student hours vs earn marks",fontsize=19)
plt.legend()
plt.show()


~~~

Program to implement univariate Linear Regression to fit a straight line using least squares.


**Developed by: sridhar c <br>
RegisterNumber: 212225040425**

## Output:
<img width="1112" height="489" alt="image" src="https://github.com/user-attachments/assets/af317111-013d-4eba-a874-9cb720510b70" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
