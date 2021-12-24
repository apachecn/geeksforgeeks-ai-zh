# 将 1D 数组转换为 2D Numpy 数组

> 原文:[https://www . geesforgeks . org/convert-a-1d-array-a-2d-numpy-array/](https://www.geeksforgeeks.org/convert-a-1d-array-to-a-2d-numpy-array/)

**Numpy** 是一个 Python 包，由多维数组对象和操作或例程的集合组成，用于对数组执行各种操作和数组的处理。这个包包含一个名为**numpy . resform**的函数，用于将一维数组转换为所需维度(n×m)的二维数组。该函数在不改变一维数组数据的情况下给出新的所需形状。

> **语法:**numpy . resform(数组，new_shape，顺序)
> 
> **参数:**
> 
> *   **数组:**是给定的一维数组，将被赋予新的形状或转换为二维数组
> *   **new_shape:** 是具有 int 或 int 元组的所需形状或二维数组
> *   **顺序**:**“C”代表 C 风格，“F”代表 Fortran 风格，“A”如果数据是 Fortran 风格，那么 Fortran 就像顺序其他 C 风格一样。**

****实施例 1:****

## **蟒蛇 3**

```
import numpy as np
# 1-D array having elements [1 2 3 4 5 6 7 8]
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Print the 1-D array
print ('Before reshaping:')
print (arr)
print ('\n')

# Now we can convert this 1-D array into 2-D in two ways

# 1\. having dimension 4 x 2
arr1 = arr.reshape(4, 2)
print ('After reshaping having dimension 4x2:')
print (arr1)
print ('\n')

# 2\. having dimension 2 x 4
arr2 = arr.reshape(2, 4)
print ('After reshaping having dimension 2x4:')
print (arr2)
print ('\n')
```

****输出:****

```
Before reshaping:
[1 2 3 4 5 6 7 8]
After reshaping having dimension 4x2:
[[1 2]
 [3 4]
 [5 6]
 [7 8]]
After reshaping having dimension 2x4:
[[1 2 3 4]
 [5 6 7 8]]
```

****例 2:让我们看到一个重要的观察，是否可以将一维数组重塑为任意二维数组。****

## **蟒蛇 3**

```
import numpy as np
# 1-D array having elements [1 2 3 4 5 6 7 8]
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Print the 1-D array
print('Before reshaping:')
print(arr)
print('\n')

# let us try to convert into 2-D array having dimension 3x3
arr1 = arr.reshape(3, 3)
print('After reshaping having dimension 3x3:')
print(arr1)
print('\n')
```

****输出:****

**![](img/949a4a808c1381608ca53d5d3232d9a4.png)**

**由此得出结论，元素的数量应等于维数的乘积，即 3×3=9，但元素总数= 8；**

****示例 3:** 另一个示例是，我们可以使用重塑方法，而无需为其中一个维度指定确切的数字。只需传递-1 作为值，NumPy 就会计算出数字。**

## **蟒蛇 3**

```
import numpy as np
# 1-D array having elements [1 2 3 4 5 6 7 8]
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Print the 1-D array
print('Before reshaping:')
print(arr)
print('\n')

arr1 = arr.reshape(2, 2, -1)
print('After reshaping:')
print(arr1)
print('\n')
```

****输出:****

```
Before reshaping:
[1 2 3 4 5 6 7 8]
After reshaping:
[[[1 2]
 [3 4]]
[[5 6]
 [7 8]]]
```