# 如何统计 NumPy 数组中唯一值的出现频率？

> 原文:[https://www . geeksforgeeks . org/如何计算 numpy 数组中唯一值的频率/](https://www.geeksforgeeks.org/how-to-count-the-frequency-of-unique-values-in-numpy-array/)

让我们看看如何计算 NumPy 数组中唯一值的频率。Python 的 numpy 库提供了 [**numpy.unique()**](https://www.geeksforgeeks.org/python-numpy-np-unique-method/) 函数来查找 numpy 数组中的唯一元素及其对应的频率。

> **语法:** numpy.unique(arr，return_counts=False)
> 
> **返回:**数组中已排序的唯一元素及其对应的频率计数 NumPy 数组。

现在，让我们看看例子:

**例 1:**

## 蟒蛇 3

```py
# import library
import numpy as np

ini_array = np.array([10, 20, 5,
                      10, 8, 20,
                      8, 9])

# Get a tuple of unique values 
# and their frequency in
# numpy array
unique, frequency = np.unique(ini_array, 
                              return_counts = True)
# print unique values array
print("Unique Values:", 
      unique)

# print frequency array
print("Frequency Values:",
      frequency)
```

**输出:**

```py
Unique Values: [ 5  8  9 10 20]
Frequency Values: [1 2 1 2 2]

```

**例 2:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a 1d-array
ini_array = np.array([10, 20, 5,
                    10, 8, 20,
                    8, 9])

# Get a tuple of unique values 
# amnd their frequency 
# in numpy array
unique, frequency = np.unique(ini_array,
                              return_counts = True) 

# convert both into one numpy array
count = np.asarray((unique, frequency ))

print("The values and their frequency are:\n",
     count)
```

**输出:**

```py
The values and their frequency are:
[[ 5  8  9 10 20]
[ 1  2  1  2  2]]
```

**例 3:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a 1d-array
ini_array = np.array([10, 20, 5,
                      10, 8, 20,
                      8, 9])

# Get a tuple of unique values 
# and their frequency in
# numpy array
unique, frequency = np.unique(ini_array, 
                              return_counts = True) 

# convert both into one numpy array 
# and then transpose it
count = np.asarray((unique,frequency )).T

print("The values and their frequency are in transpose form:\n",
     count)
```

**输出:**

```py
The values and their frequency are in transpose form:
[[ 5  1]
[ 8  2]
[ 9  1]
[10  2]
[20  2]]
```