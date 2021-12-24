# 如何将字典转换成 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何将字典转换为 numpy 数组/](https://www.geeksforgeeks.org/how-to-convert-a-dictionary-into-a-numpy-array/)

有时需要将 Python 中的[字典](https://www.geeksforgeeks.org/python-dictionary/)转换成 NumPy 数组，Python 提供了一种有效的方法来执行这个操作。将字典转换为 NumPy 数组会产生一个保存字典中键值对的数组。Python 提供了 **numpy.array()** 方法来将字典转换为 numpy 数组，但是在应用这个方法之前，我们必须做一些前置任务。作为前期任务，请遵循以下三个简单步骤

1.  首先调用****dict . items()**返回字典中的一组键值对。**
2.  **然后使用 **列表(obj)** 以此组为对象将其转换为列表。**
3.  **最后以此列表为数据调用**numpy . array(data)**将其转换为数组。**

> ****语法:****
> 
> ****numpy . array(**)T2【对象】 **、** *dtype = None* **、** *** **、** *copy = True* **、** *order = 'K'* **、** *subok = False* **、** *ndmin = 0* 【T28**
> 
>  ****参数:**
> 
> **对象:**一个数组，任何暴露数组接口的对象
> 
> **数据类型:**数组所需的数据类型。
> 
> **复制:**如果为真(默认)，则复制对象。否则，只有当 __array__ 返回副本时，才会创建副本
> 
> **顺序:**指定阵列的内存布局
> 
> **subok** :如果为真，则传递子类，否则返回的数组强制为基类数组(默认)
> 
> **ndmin:** 指定结果数组应具有的最小维数。
> 
> **返回:**
> 
> **n 数组:**满足指定要求的数组对象。**

****例 1:****

## **计算机编程语言**

```
# Python program to convert
# dictionary to numpy array

# Import required package
import numpy as np

# Creating a Dictionary
# with Integer Keys
dict = {1: 'Geeks',
        2: 'For',
        3: 'Geeks'}

# to return a group of the key-value
# pairs in the dictionary
result = dict.items()

# Convert object to a list
data = list(result)

# Convert list to an array
numpyArray = np.array(data)

# print the numpy array
print(numpyArray)
```

****输出:****

```
[['1' 'Geeks']
 ['2' 'For']
 ['3' 'Geeks']] 
```

****例 2:****

## **计算机编程语言**

```
# Python program to convert
# dictionary to numpy array

# Import required package
import numpy as np

# Creating a Nested Dictionary
dict = {1: 'Geeks',
        2: 'For',
        3: {'A': 'Welcome',
            'B': 'To',
            'C': 'Geeks'}
        }

# to return a group of the key-value
# pairs in the dictionary
result = dict.items()

# Convert object to a list
data = list(result)

# Convert list to an array
numpyArray = np.array(data)

# print the numpy array
print(numpyArray)
```

****输出:****

```
[[1 'Geeks']
 [2 'For']
 [3 {'A': 'Welcome', 'B': 'To', 'C': 'Geeks'}]] 
```

****例 3:****

## **计算机编程语言**

```
# Python program to convert
# dictionary to numpy array

# Import required package
import numpy as np

# Creating a Dictionary
# with Mixed keys
dict = {'Name': 'Geeks',
        1: [1, 2, 3, 4]}

# to return a group of the key-value
# pairs in the dictionary
result = dict.items()

# Convert object to a list
data = list(result)

# Convert list to an array
numpyArray = np.array(data)

# print the numpy array
print(numpyArray)
```

****输出:****

```
[['Name' 'Geeks']
 [1 list([1, 2, 3, 4])]] 
```