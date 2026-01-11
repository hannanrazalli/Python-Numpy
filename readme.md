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

# Array indexing
arr = np.array([1, 2, 3, 4])
print(arr[0])

arr = np.array([1, 2, 3, 4])
print(arr[2] + arr[3]) *Maths in array*

arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])
print('2nd element on 1st row: ', arr[0, 1])

a = np.array([[1,2,3,4],[5,6,7,8]])
print(a[0,1]) *How to access 2-D element*

a = np.array([[[1,2,3],[4,5,6]],[[7,8,9],[10,11,12]]])
print(a[1,0,2]) *How to access 3-D element*

arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])
print('Last element from 2nd dim: ', arr[1, -1]) *Negative indexing*