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

# Slicing arrays
arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[1:5]) *Implicit slicing*

arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[4:]) *End slicing*

arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[:4]) *Front slicing*

arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[-3:-1]) *Negative slicing*

arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[1:5:2]) *Step slicing*

arr = np.array([1, 2, 3, 4, 5, 6, 7])
print(arr[::2]) *Return all with step 2*

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])
print(arr[1, 1:4]) *2-D aray: Slice 2nd element*

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])
print(arr[0:2, 2]) *2-D array: Slice both elements, return index 2*

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])
print(arr[0:2, 1:4]) *Slice 2-D array, return 2-D array*


# Numpy Data Type
i - integer
b - boolean
u - unsigned integer
f - float
c - complex float
m - timedelta
M - datetime
O - object
S - string
U - unicode string
V - fixed chunk of memory for other type ( void )

arr = np.array([1, 2, 3, 4])
print(arr.dtype) *Print data type*

arr = np.array([1, 2, 3, 4], dtype='S') *Set data type of String*
print(arr)
print(arr.dtype)

result:
[b'1' b'2' b'3' b'4'] *b means byte*
|S1

arr = np.array([1.1, 2.1, 3.1])
newarr = arr.astype('i') *Convert to integer*
print(newarr)
print(newarr.dtype)

RESULT:
[1 2 3]
int32

arr = np.array([1, 0, 3])
newarr = arr.astype(bool) *Converts to boolean*
print(newarr)
print(newarr.dtype)


# Copy & View array
arr = np.array([1, 2, 3, 4, 5])
x = arr.copy() *Copy array*
arr[0] = 42
print(arr)
print(x)


arr = np.array([1, 2, 3, 4, 5])
x = arr.view() *View array*
arr[0] = 42
print(arr)
print(x)


arr = np.array([1, 2, 3, 4, 5])
x = arr.copy()
y = arr.view()
print(x.base) *None*
print(y.base) *[1 2 3 4 5]*
*Check if array owns its data*

# Reshaping arrays: 1-D to 2-D
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
newarr = arr.reshape(4, 3) *4 rows, 3 columns*
print(newarr)

# Reshaping arrays: 1-D to 3-D
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
newarr = arr.reshape(2, 3, 2)
*2 dimensions, 3 rows, 2 columns*
print(newarr)

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])
print(arr.reshape(2, 4).base)
*If returns original array, means it is a view*

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])
newarr = arr.reshape(2, 2, -1)
*Reshape to 2 dimensions, 2 rows and automatic columns based on balance*
print(newarr)

arr = np.array([[1, 2, 3], [4, 5, 6]])
newarr = arr.reshape(-1)
*Flatten 2-D array to 1-D array*
print(newarr)

