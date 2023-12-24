# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1.Interchange and equation (or ).
2.Divide the equation by (or ).
3.Add times the equation to the equation (or ). Add times the equation to the equation (or ).
4.Multiply the equation by (or ).
```
## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: PULI NAGA NEERAJ
RegisterNumber: 23004033
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
        sys.exit('Divide by zero detected')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
             a[j][k]=a[j][k]-ratio*a[i][k]
X[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,X[i]), end=' ')
```

## Output:
![image](https://github.com/PuliNagaNeeraj/Gaussian/assets/138849173/a89c2239-14b6-42de-a4e1-8ea3863009df)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

