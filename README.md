# Programming Assignment 2: Numerical Python (NumPy)
This repository contains solutions to two basic data preprocessing problems using NumPy: Normalization and Finding Elements Divisible by 3. These problems are designed to practice basic data manipulation and saving results to files in Python.

## Overview
### 1. Normalization Problem: 
**Objective:** Normalize a 5x5 NumPy array of random numbers.
Normalization is a key preprocessing step in data analytics that involves centering and scaling the data. Centering means subtracting the mean, and scaling means dividing by the standard deviation.

**Process:**
1. Create a 5x5 array with random numbers.
2. Normalize the array using the formula: 𝑍 = 𝑋 − mean/std
3. Save the normalized array to X_normalized.npy.

### 2. Divisible by 3 Problem: 
**Objective:** Find elements divisivle by 3 from a 10x10 NumPy array of squares of the first 100 positive integers.

**Process:** 
1. Generate a 10x10 matrix where each elements is the square of an integer from 1 to 100.
2. Extract all elements that are visible by 3.
3. Save the array of elements divisible by 3 as div_by_3.npy.

# How to Run
### 1. Normalization Problem:
* Run the code that generates a 5x5 random array and normalizes it.
* The normalized data will be saved as X_normalized.npy.
  
Code:
```python
import numpy as np

# Generate a 5x5 array of random numbers
X = np.random.random((5,5))

# Define a function to normalize the input array
def normalization(z):
    # Calculate the mean of the array
    m = z.mean()
    # Calculate the standard deviation of the array
    s = z.std()
    # Normalize the input array using the formula (z - mean) / std_dev
    Z = (z - m) / s
    # Return the normalized array
    return Z

# Normalize the random array X
X_normalized = normalization(X)
# Save the normalized array to a .npy file
np.save('X_normalized.npy', X_normalized)
```

### 2. Divisible by 3
* Run the code that generates a 10x10 array of squares of integers and finds elements divisible by 3.
* The filtered array will be saved as div_by_3.npy.

Code:

```python
import numpy as np

# Create an array of squares from 1 to 100 in a 10x10 matrix
x = (np.arange(1, 101) ** 2).reshape(10, 10)

# Initialize an empty list to store squares divisible by 3
squares_div_by_3 = x[x % 3 == 0]

# Save the NumPy array to a file named 'div_by_3.npy'
np.save('div_by_3.npy', squares_div_by_3)
```
### Metadata
* **Name:** Cueco, Czarina Julia C.
* **Section:** 2ECE-B
* **Date Submitted:** September 2, 2024 (Edited: 09/05/24)
