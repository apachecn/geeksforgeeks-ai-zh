# Python |在 numpy 中查找范围内的元素

> 原文:[https://www . geesforgeks . org/python-find-elements-in-range-in-numpy/](https://www.geeksforgeeks.org/python-find-elements-within-range-in-numpy/)

给定 numpy 数组，任务是找到特定范围内的元素。让我们讨论一些做这项任务的方法。

**方法一:使用`np.where()`**

```
# python code to demonstrate
# finding elements in range
# in numpy array
import numpy as np

ini_array = np.array([1, 2, 3, 45, 4, 7, 810, 9, 6])

# printing initial array
print("initial_array : ", str(ini_array));

# find elements in range 6 to 10
result = np.where(np.logical_and(ini_array>= 6, ini_array<= 10))

# printing result
print("resultant_array : ", result)
```

**Output:**

```
initial_array :  [  1   2   3  45   4   7 810   9   6]
resultant_array :  (array([5, 7, 8]),)

```

**方法 2:使用`numpy.searchsorted()`**

```
# Python code to demonstrate
# finding elements in range
# in numpy array

import numpy as np

ini_array = np.array([1, 2, 3, 45, 4, 7, 9, 6])

# printing initial array
print("initial_array : ", str(ini_array));

# find elements in range 6 to 10
start = np.searchsorted(ini_array, 6, 'left')
end = np.searchsorted(ini_array, 10, 'right')
result = np.arange(start, end)

# printing result
print("resultant_array : ", result)
```

**Output:**

```
initial_array :  [ 1  2  3 45  4  7  9  6]
resultant_array :  [5 6 7]

```

**方法#3:使用***

```
# Python code to demonstrate
# finding elements in range
# in numpy array

import numpy as np

ini_array = np.array([1, 2, 3, 45, 4, 7, 9, 6])

# printing initial array
print("initial_array : ", str(ini_array));

# find elements in range 6 to 10
result = ini_array[(ini_array>6)*(ini_array<10)]

# printing result
print("resultant_array : ", result)
```

**Output:**

```
initial_array :  [ 1  2  3 45  4  7  9  6]
resultant_array :  [7 9]

```