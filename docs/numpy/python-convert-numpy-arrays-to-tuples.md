# Python |将 Numpy 数组转换为元组

> 原文:[https://www . geeksforgeeks . org/python-convert-numpy-arrays-to-tuples/](https://www.geeksforgeeks.org/python-convert-numpy-arrays-to-tuples/)

给定一个 numpy 数组，编写一个程序将 numpy 数组转换成元组。
**示例–**

```
Input: ([[1, 0, 0, 1, 0], [1, 2, 0, 0, 1]])
Output:  ((1, 0, 0, 1, 0), (1, 2, 0, 0, 1))

Input:  ([['manjeet', 'akshat'], ['nikhil', 'akash']])
Output:  (('manjeet', 'akshat'), ('nikhil', 'akash'))
```

下面给出了将 numpy 数组转换为元组的各种方法。
**方法#1:使用元组和映射**

## 蟒蛇 3

```
# Python code to demonstrate
# deletion of columns from numpy array

import numpy as np

# initialising numpy array
ini_array = np.array([['manjeet', 'akshat'], ['nikhil', 'akash']])

# convert numpy arrays into tuples
result = tuple(map(tuple, ini_array))

# print result
print ("Resultant Array :"+str(result))
```

**输出:**

```
Result:(('manjeet', 'akshat'), ('nikhil', 'akash'))
```

**方法 2:使用天真方法**

## 蟒蛇 3

```
# Python code to demonstrate
# deletion of columns from numpy array

import numpy as np

# initialising numpy array
ini_array = np.array([['manjeet', 'akshat'], ['nikhil', 'akash']])

# convert numpy arrays into tuples
result = tuple([tuple(row) for row in ini_array])

# print result
print ("Result:"+str(result))
```

**输出:**

```
Result:(('manjeet', 'akshat'), ('nikhil', 'akash'))
```