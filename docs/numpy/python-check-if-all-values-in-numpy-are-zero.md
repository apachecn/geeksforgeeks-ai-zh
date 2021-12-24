# Python |检查 numpy 中的所有值是否为零

> 原文:[https://www . geesforgeks . org/python-检查 numpy 中的所有值是否为零/](https://www.geeksforgeeks.org/python-check-if-all-values-in-numpy-are-zero/)

给定一个 numpy 数组，任务是检查 numpy 数组是否包含全零。让我们讨论几个解决上述任务的方法。
**方法#1:** 使用 numpy.count _ 非零()
获取零的计数

## 蟒蛇 3

```
# Python code to demonstrate
# to count the number of elements
# in numpy which are zero

import numpy as np

ini_array1 = np.array([1, 2, 3, 4, 5, 6, 0])
ini_array2 = np.array([0, 0, 0, 0, 0, 0])

# printing initial arrays
print("initial arrays", ini_array1)
print(ini_array2)

# code to find whether all elements are zero
countzero_in1 = np.count_nonzero(ini_array1)
countzero_in2 = np.count_nonzero(ini_array2)

# printing result
print("Number of non-zeroes in array1 : ", countzero_in1)
print("Number of non-zeroes in array2 : ", countzero_in2)
```

**Output:** 

```
initial arrays [1 2 3 4 5 6 0]
[0 0 0 0 0 0]
Number of non-zeroes in array1 :  6
Number of non-zeroes in array2 :  0
```

**方法 2:** 使用 numpy.any()

## 蟒蛇 3

```
# Python code to check that whether
# all elements in numpy are zero

import numpy as np

ini_array1 = np.array([1, 2, 3, 4, 5, 6, 0])
ini_array2 = np.array([0, 0, 0, 0, 0, 0])

# printing initial arrays
print("initial arrays", ini_array1)

# code to find whether all elements are zero
countzero_in1 = not np.any(ini_array1)
countzero_in2 = not np.any(ini_array2)

# printing result
print("Whole array contains zeroes in array1 ?: ", countzero_in1)
print("Whole array contains zeroes in array2 ?: ", countzero_in2)
```

**Output:** 

```
initial arrays [1 2 3 4 5 6 0]
Whole array contains zeroes in array1 ?:  False
Whole array contains zeroes in array2 ?:  True
```