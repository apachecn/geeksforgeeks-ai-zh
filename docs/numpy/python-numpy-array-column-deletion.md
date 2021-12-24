# Python–Numpy 数组列删除

> 原文:[https://www . geesforgeks . org/python-numpy-array-column-delete/](https://www.geeksforgeeks.org/python-numpy-array-column-deletion/)

给定一个 numpy 数组，编写一个程序从 numpy 数组中删除列。

**示例–**

```
Input: [['akshat', 'nikhil'], ['manjeeet', 'akash']]
Output:  [['akshat']['manjeeet']]

Input:  [[1, 0, 0, 1, 0], [0, 1, 2, 1, 1]]
Output:  [[1 0 1 0][0 2 1 1]]

```

下面给出了从 numpy 数组中删除列的各种方法。

**方法#1:使用 np.delete()**

```
# Python code to demonstrate
# deletion of columns from numpy array

import numpy as np

# initialising numpy array
ini_array = np.array([[1, 0, 0, 1, 0],
                        [0, 1, 2, 1, 1]])

# deleting second column from array
result = np.delete(ini_array, 1, 1)

# print result
print ("Resultant Array :"+str(result))
```

**输出:**

```
Resultant Array :[[1 0 1 0]
 [0 2 1 1]]

```

**方法 2:使用压缩()和逻辑 _ 非()**

```
# Python code to demonstrate
# deletion of columns from numpy array

import numpy as np

# initialising numpy array
ini_array = np.array([[1, 0, 0, 1, 0], [1, 2, 0, 0, 1]])
z = [False, True, False, False, False]

# deleting second column from array
result = ini_array.compress(np.logical_not(z), axis = 1)

# print result
print ("Resultant Array :"+str(result))
```

**输出:**

```
Resultant Array :[[1 0 1 0]
 [1 0 0 1]]

```

**方法#3:使用 logical_not()**

```
# Python code to demonstrate
# deletion of columns from numpy array

import numpy as np

# initialising numpy array
ini_array = np.array([[1, 0, 0, 1, 0], [1, 2, 0, 0, 1]])
z = [False, True, False, False, False]

# deleting second column from array
result = ini_array[:, np.logical_not(z)]

# print result
print ("Resultant Array :"+str(result))
```

**输出:**

```
Resultant Array :[[1 0 1 0]
 [1 0 0 1]]

```