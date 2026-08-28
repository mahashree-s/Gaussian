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
<img width="788" height="843" alt="image" src="https://github.com/user-attachments/assets/375db87b-a7a9-4970-a9da-f35847fc33d7" />


## Output:

<img width="986" height="530" alt="image" src="https://github.com/user-attachments/assets/4c1c6c09-81a0-4f99-a4f8-a167d2596384" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

