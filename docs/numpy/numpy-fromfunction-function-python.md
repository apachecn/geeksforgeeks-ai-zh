# numpy.fromfunction()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-from function-function-python/](https://www.geeksforgeeks.org/numpy-fromfunction-function-python/)

**numpy.fromfunction()** 函数通过在每个坐标上执行一个函数来构造一个数组，因此得到的数组在坐标(x，y，z)处有一个值 fn(x，y，z)。

> 语法:numpy.fromfunction(函数、形状、数据类型)
> 
> 参数:
> 
> 【可调用】函数:用 N 个参数调用函数，其中 N 是形状的秩。每个参数代表沿着特定轴变化的阵列坐标。
> 
> shape : [(N，)元组的 ints]输出数组的 shape，它也决定传递给函数的坐标数组的形状。
> 
> 数据类型:[数据类型，可选]传递给函数的坐标数组的数据类型。
> 
> 返回:输出数组。

代码#1:

## 蟒蛇 3

```
# Python program explaining
# numpy.fromfunction() function

# importing numpy as geek
import numpy as geek

gfg = geek.fromfunction(lambda i, j: i * j, (4, 4), dtype = float)

print(gfg)
```

输出:

> [[0\. 0\. 0\. 0.]
> 
> [0\. 1\. 2\. 3.]
> 
> [0\. 2\. 4\. 6.]
> 
> [0\. 3\. 6\. 9.]]

代码#2:

## 蟒蛇 3

```
# Python program explaining
# numpy.fromfunction() function

# importing numpy as geek
import numpy as geek

gfg = geek.fromfunction(lambda i, j: i == j, (3, 3), dtype = int)

print(gfg)
```

输出:

> [[真假假]
> 
> [假真假]
> 
> [假假真]]