# Python |从浮点数数组中过滤出整数

> 原文:[https://www . geesforgeks . org/python-filter-out-整数-from-float-numpy-array/](https://www.geeksforgeeks.org/python-filter-out-integers-from-float-numpy-array/)

给定一个 numpy 数组，任务是从包含浮点数和整数的数组中过滤出整数。让我们看看解决给定任务的几种方法。
**方法#1:使用 a 型(int)**

## 蟒蛇 3

```
# Python code to demonstrate
# filtering integers from numpy array
# containing integers and float

import numpy as np

# initialising array
ini_array = np.array([1.0, 1.2, 2.2, 2.0, 3.0, 2.0])

# printing initial array
print ("initial array : ", str(ini_array))

# filtering integers
result = ini_array[ini_array != ini_array.astype(int)]

# printing resultant
print ("final array", result)
```

**Output:** 

```
initial array :  [ 1\.   1.2  2.2  2\.   3\.   2\. ]
final array [ 1.2  2.2]
```

**方法 2:使用 np.equal()和 np.mod()**

## 蟒蛇 3

```
# Python code to demonstrate
# filtering integers from numpy array
# containing integers and float

import numpy as np

# initialising array
ini_array = np.array([1.0, 1.2, 2.2, 2.0, 3.0, 2.0])

# printing initial array
print ("initial array : ", str(ini_array))

# filtering integers
result = ini_array[~np.equal(np.mod(ini_array, 1), 0)]

# printing resultant
print ("final array : ", str(result))
```

**Output:** 

```
initial array :  [ 1\.   1.2  2.2  2\.   3\.   2\. ]
final array :  [ 1.2  2.2]
```

**方法三:使用**

## 蟒蛇 3

```
# Python code to demonstrate
# filtering integers from numpy array
# containing integers and float

import numpy as np

# initialising array
ini_array = np.array([1.0, 1.2, 2.2, 2.0, 3.0, 2.0])

# printing initial array
print ("initial array : ", str(ini_array))

# filtering integers
mask = np.isclose(ini_array, ini_array.astype(int))
result = ini_array[~mask]

# printing resultant
print ("final array : ", str(result))
```

**Output:** 

```
initial array :  [ 1\.   1.2  2.2  2\.   3\.   2\. ]
final array :  [ 1.2  2.2]
```