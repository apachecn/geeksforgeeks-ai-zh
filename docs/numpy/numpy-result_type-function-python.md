# numpy.result_type()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-result _ type-function-python/](https://www.geeksforgeeks.org/numpy-result_type-function-python/)

**`numpy.result_type()`** 函数返回将 **NumPy 类型提升**规则应用于参数后得到的类型。

**NumPy 类型提升举例:**
假设计算 3*arr，其中 arr 是 32 位浮点的数组，直观上应该会得到 32 位浮点输出。如果 3 是 32 位整数，NumPy 规则表明它不能无损地转换成 32 位浮点，因此结果类型应该是 64 位浮点。

> **语法:**numpy . result _ type(arrays _ and _ dtypes)
> 
> **参数:**
> **数组 _ 和 _ 数据类型:**【数组和数据类型列表】需要结果类型的某个运算的操作数。
> **返回:**【数据类型】返回结果类型。

**代码#1 :**

```py
# Python program explaining
# numpy.result_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.result_type('f4', 'i8')

print (gfg)
```

**输出:**

```py
float64

```

**代码#2 :**

```py
# Python program explaining
# numpy.result_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.result_type(3, geek.arange(7, dtype = 'i1'))

print (gfg)
```

**输出:**

```py
int8

```