# 使用 Python 中的 NumPy 计算一维数组向量的内积

> 原文:[https://www . geeksforgeeks . org/使用 python 中的 numpy 计算一维数组的向量内积/](https://www.geeksforgeeks.org/compute-the-inner-product-of-vectors-for-1-d-arrays-using-numpy-in-python/)

Python 有一个流行的包，叫做 NumPy，用来对一维和多维数组进行复杂的计算。要求两个数组的内积，可以使用 NumPy 包的 [inner()](https://www.geeksforgeeks.org/numpy-inner-in-python/) 函数。

> **语法:** numpy.inner(array1，array2)
> 
> **参数:**
> 
> **数组 1，数组 2:** 要评估的数组
> 
> **返回:**两个数组的内积

**例 1:**

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 1-D arrays
array1 = np.array([6,2])
array2 = np.array([2,5])

print("Original 1-D arrays:")
print(array1)
print(array2)

# Output
print("Inner Product of the two array is:")
result = np.inner(array1, array2)
print(result)
```

**输出:**

```
Original 1-D arrays:
[6 2]
[2 5]
Inner Product of the two array is:
22

```

**例 2:**

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 1-D arrays
array1 = np.array([1,3,5])
array2 = np.array([0,1,5])

print("Original 1-D arrays:")
print(array1)
print(array2)

# Output
print("Inner Product of the two array is:")
result = np.inner(array1, array2)
print(result)
```

**输出:**

```
Original 1-D arrays:
[1 3 5]
[0 1 5]
Inner Product of the two array is:
28

```

**例 3:**

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 1-D arrays
array1 = np.array([1,2,2,8])
array2 = np.array([2,1,0,6])

print("Original 1-D arrays:")
print(array1)
print(array2)

# Output
print("Inner Product of the two array is:")
result = np.inner(array1, array2)
print(result)
```

**输出:**

```
Original 1-D arrays:
[1 2 2 8]
[2 1 0 6]
Inner Product of the two array is:
52

```