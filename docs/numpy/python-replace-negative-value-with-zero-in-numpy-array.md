# Python |在 numpy 数组中用零替换负值

> 原文:[https://www . geeksforgeeks . org/python-在 numpy 数组中用零替换负值/](https://www.geeksforgeeks.org/python-replace-negative-value-with-zero-in-numpy-array/)

给定 numpy 数组，任务是在 numpy 数组中用零替换负值。让我们看看这个问题的几个例子。

**方法#1:天真法**

```
# Python code to demonstrate
# to replace negative value with 0
import numpy as np

ini_array1 = np.array([1, 2, -3, 4, -5, -6])

# printing initial arrays
print("initial array", ini_array1)

# code to replace all negative value with 0
ini_array1[ini_array1<0] = 0

# printing result
print("New resulting array: ", ini_array1)
```

**输出:**

```
initial array [ 1  2 -3  4 -5 -6]
New resulting array:  [1 2 0 4 0 0]

```