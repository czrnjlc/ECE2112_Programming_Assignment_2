# Programming Assignment 2: Data Normalization and Filtering
## Overview
This repository contains Python scripts for two data processing tasks:

### 1. Normalization Problem: 
This script creates a 5x5 NumPy array of random numbers, normalizes it, and saves the result to a file.
### 2. Divisible by 3 Problem: 
This script creates a 10x10 NumPy array of squares of the first 100 positive integers, filters out elements divisible by 3, and saves these elements to a file.

## Scripts
### 1. Normalization
#### Objective: Generate a 5x5 array of random numbers, normalize it, and save the result.
#### Process:
1. Create a 5x5 array with random numbers.
2. Normalize the array using the formula: 𝑍 = 𝑋 − mean/std
3. Save the normalized array to X_normalized.npy.

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
#### Objective: Create a 10x10 array of squares from 1 to 100, filter elements divisible by 3, and save the result.
#### Process:
1. Generate a 10x10 array with squares of the first 100 integers.
2. Filter elements that are divisible by 3.
3. Save these elements to div_by_3.npy.

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
#### Name: Cueco, Czarina Julia C.
#### Section: 2ECE-B
#### Date Submitted: September 2, 2024
