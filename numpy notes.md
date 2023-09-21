# Numpy Notes 
# Vocab:
  1. Numpy: a python library for numerical and mathematical operations. It provides, multi-dimensional arrays and matrices, along with a wide range of mathematical functions to operate on these arrays efficiently. 
  2. Array: The fundamental data structure in NumPy. An array is a collection of elements of the same data type organized in a grid with dimensions defined by its shape.
  3. Shape: The dimensions (number of rows and columns) of a NumPy array. It is represented as a tuple.
  4. Element: A single value in a NumPy array. Elements can be accessed and manipulated individually or in groups.
  5. dtype (Data Type): The data type of the elements in a NumPy array, which can be int, float, bool, etc. NumPy provides several data types with varying levels of precision.
  6. Vector: A one-dimensional array. In NumPy, vectors are often represented as arrays with a single row or column.
  7. Matrix: A two-dimensional array with rows and columns. Matrices are used for various mathematical operations.
  8. Dimension: The number of axes (dimensions) in an array. For example, a 1D array has one dimension, a 2D array (matrix) has two dimensions, and so on.
  9. Indexing: Accessing individual elements or subarrays within a NumPy array using square brackets and indices. NumPy uses zero-based indexing.
  10. Slicing: Extracting a portion (subarray) of an array by specifying a range of indices. Slicing allows you to work with a subset of the data.
  11. Broadcasting: NumPy's mechanism for performing element-wise operations on arrays with different shapes, making it easier to work with arrays of different sizes.
  12. Vectorization: The process of performing operations on entire arrays rather than using explicit loops. NumPy encourages vectorized operations, which are more efficient and concise.
  13. Element-wise Operations: Operations performed on corresponding elements of two or more arrays. For example, addition, subtraction, multiplication, and division can be done element-wise.
  14. Aggregation: Calculating summary statistics of an array, such as mean, median, sum, min, and max.
  15. Universal Functions (ufuncs): NumPy functions that operate element-wise on arrays, allowing for efficient and fast computation. Examples include np.add(), np.multiply(), and np.sin().
  16. Reshaping: Changing the shape (dimensions) of an array using methods like reshape(), flatten(), and ravel().
  17. Concatenation: Combining two or more arrays along specified axes (dimensions) using functions like np.concatenate() and np.stack().
  18. Transpose: Switching the rows and columns of a matrix using the T attribute or np.transpose() function.
  19. Masking: Using boolean arrays to filter, select, or modify elements based on a certain condition.
  20. NumPy Functions: Familiarize yourself with key NumPy functions and methods like np.sum(), np.mean(), np.max(), np.min(), np.dot(), np.linalg for linear algebra, and more.
  21. Random Number Generation: NumPy provides functions in the np.random module for generating random numbers and random arrays.
  22. Numpy zeros makes an array filled with zeros. It takes the shape of the array as an argument and returns an array of zeros with the specified shape.
  23. Identity matrix: a specific type of square matrix where all the elements along its main diagonal (from the top-left to the bottom-right) are equal to 1, and all other elements are equal to 0. 

# installation
pip install numpy

# import numpy
import numpy as np 

# to create an array
a = np.array([1, 2, 3, 4, 5])

# Creates a 3x4 array filled with zeros
zeros_array = np.zeros((3, 4))

# Creates a 2x3 array filled with ones
ones_array = np.ones((2, 3))       

 # Creates a 3x3 array with random values
random_array = np.random.rand(3, 3) 

# Creates a range of values: [0,2,4,6,8] 
range_array = np.arange(0, 10, 2)

# Creates an array with 5 evenly spaced values between 0 and 1
linspace_array = np.linspace(0, 1, 5)

# Array operations
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

c = a + b
d = a * b

# Indexing and Slicing
arr = np.array([0, 1, 2, 3, 4, 5])
print(arr[2])       # Access element at index 2
print(arr[2:5])     # Get a slice from index 2 to 4

# Reshaping Arrays: you can reshape it using the shape  and the reshape() attribute.
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr.shape)           # Prints the shape (2, 3)
reshaped_arr = arr.reshape(3, 2)  # Reshape to (3, 2)

# Array Functions 
arr = np.array([1, 2, 3, 4, 5])
print(np.sum(arr))        # Sum of array elements
print(np.mean(arr))       # Mean of array elements
print(np.max(arr))        # Maximum value in the array

# Array Broadcasting

# Advanced Operations

# Documentation and Resources

# Create a 2x3 array filled with zeros
zeros_array = np.zeros((2, 3))
print(zeros_array)

# Create a 4x4 identity matrix
identity_matrix = np.eye(4)
print(identity_matrix)


