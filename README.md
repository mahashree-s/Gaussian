# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

### Step 1:

Import the `os`, `numpy`, and `sys` modules. Set `OPENBLAS_NUM_THREADS` to `1` for NumPy operations.

### Step 2:

Read the number of unknowns from the user and create NumPy arrays to store the **augmented matrix** and the **solution vector**. Then read the coefficients of the augmented matrix as input.

### Step 3:

Apply **Gaussian Elimination** by converting the augmented matrix into upper triangular form. Calculate the elimination ratio and update the matrix elements. If a zero pivot is detected, terminate the program with a divide-by-zero message.

### Step 4:

Perform **back substitution** to calculate the values of the unknowns. Store the solutions in `x` and print each value in the format `X0`, `X1`, etc., rounded to two decimal places.

## Program:
Program to find the solution of a matrix using Gaussian Elimination.
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: MAHASHREE S
RegisterNumber: 212225230163
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np
import sys

n = int(input())

a = np.zeros((n, n+1))
x = np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())

for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')

    for j in range(i+1, n):
        ratio = a[j][i] / a[i][i]

        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

x[n-1] = a[n-1][n] / a[n-1][n-1]

for i in range(n-2, -1, -1):
    x[i] = a[i][n]

    for j in range(i+1, n):
        x[i] = x[i] - a[i][j] * x[j]

    x[i] = x[i] / a[i][i]

for i in range(n):
    print('X%d = %0.2f' % (i, x[i]), end=' ')
```

## Output:

<img width="986" height="530" alt="image" src="https://github.com/user-attachments/assets/4c1c6c09-81a0-4f99-a4f8-a167d2596384" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

