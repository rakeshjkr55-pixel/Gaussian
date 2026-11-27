# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Read n, matrix A, and vector B; initialize solution vector X.
2. Convert A to upper triangular form using forward elimination.
3. Compute unknowns using back substitution.
4. Print the solution vector X.

```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber:
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f ' % (i,x[i]),end='')

*/
```

## Output:
<img width="1247" height="583" alt="Screenshot 2026-11-27 092050" src="https://github.com/user-attachments/assets/82faad66-da77-4fdc-95b7-f73abf9e1aae" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

