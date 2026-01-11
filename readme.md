# Making list array
import numpy as np

arr = np.array([1,2,3,4,5]) *List*
arr = np.array((1,2,3,4,5)) *Tuple*
print(arr)
print(np.__version__)
print(type(arr)) *print type of array*

a = np.array(42) *0-D array*
a = np.array([1, 2, 3, 4, 5]) *1-D array*
a = np.array([[1,2,3,4],[5,6,7,8]]) *2-D array*
a = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]]) *3-D array*

# Checking array dimension
a = np.array(42)
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(a.ndim)
print(b.ndim)
print(c.ndim)
print(d.ndim)

# Giving number of dimension
a = np.array([1,2,3,4], ndmin=5)

print(a)
print('Number of dimensions:', a.ndim)