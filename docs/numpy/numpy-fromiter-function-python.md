# numpy.fromiter()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-from ITER-function-python/](https://www.geeksforgeeks.org/numpy-fromiter-function-python/)

**numpy.fromiter()** 函数从可迭代对象创建一个新的一维数组。

> **语法:** numpy.fromiter(iterable，dtype，count = -1)
> 
> **参数:**
> 
> **可迭代:**【可迭代对象】为数组提供数据的可迭代对象。
> 
> **数据类型:**【数据类型】返回数组的数据类型。
> 
> **计数:**【int，可选】要读取的项目数。
> 
> **返回:**【n 数组】输出数组。

**代码#1 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.fromiter() function 

# importing numpy as geek 
import numpy as geek

iterable = (x * x*x for x in range(4))

gfg = geek.fromiter(iterable, int)

print (gfg)
```

**输出:**

> [ 0  1  8 27]

**代码#2 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.fromiter() function 

# importing numpy as geek 
import numpy as geek

iterable = (x * x for x in range(6))

gfg = geek.fromiter(iterable, float)

print (gfg)
```

**输出:**

> [ 0\.  1\.  4\.  9\. 16\. 25.]