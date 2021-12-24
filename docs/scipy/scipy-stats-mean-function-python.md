# sciPy stats.mean()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-mean-function-python/](https://www.geeksforgeeks.org/scipy-stats-mean-function-python/)

`**scipy.stats.mean(array, axis=0)**`函数计算数组元素沿数组指定轴的算术平均值(python 中的 list)。

是公式–
![](img/a66fab605678af4a57b07c619882c187.png)

> **参数:**
> **数组:**输入有计算算术平均值元素的数组或对象。
> **轴:**计算平均值的轴。默认情况下，轴= 0
> 
> **返回:**基于设置参数的数组元素的算术平均值。

**代码#1:**

```
# Arithmetic Mean 

import scipy

arr1 = scipy.mean([1, 3, 27]) 

print("Arithmetic Mean is :", arr1) 
```

**Output:**

```
Arithmetic Mean is : 10.3333333333

```

**代码#2:** 多维数据

```
# Arithmetic Mean 

from scipy import mean

arr1 = [[1, 3, 27], 
        [3, 4, 6], 
        [7, 6, 3], 
        [3, 6, 8]] 

print("Arithmetic Mean is :", mean(arr1)) 

# using axis = 0
print("\nArithmetic Mean is with default axis = 0 : \n", 
      mean(arr1, axis = 0))

# using axis = 1
print("\nArithmetic Mean is with default axis = 1 : \n", 
      mean(arr1, axis = 1))  
```

**Output:**

```
Arithmetic Mean is : 6.41666666667

Arithmetic Mean is with default axis = 0 : 
 [  3.5    4.75  11\.  ]

Arithmetic Mean is with default axis = 1 : 
 [ 10.33333333   4.33333333   5.33333333   5.66666667]

```