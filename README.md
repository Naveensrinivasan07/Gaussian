# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.  Import numpy as np
2. From sys package import Guassian
3. Get input from the user
4.   Print result
## Program:
```
Developed by:NAVEEN S
RegisterNumber: 212222240070
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exist('Divide by zero found')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
X[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i]=a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,X[i]),end=' ')
```
## Output:
![ex6(mfa)(1)](https://github.com/Naveensrinivasan07/Gaussian/assets/119475891/ca47b1c8-2b2e-43c5-a8ad-4df0058ab545)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

