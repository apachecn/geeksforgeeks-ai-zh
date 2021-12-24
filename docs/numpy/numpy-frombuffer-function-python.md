# numpy.frombuffer()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-from buffer-function-python/](https://www.geeksforgeeks.org/numpy-frombuffer-function-python/)

numpy.frombuffer()函数将缓冲区解释为一维数组。

> **语法:** numpy.frombuffer(buffer，dtype = float，count = -1，offset = 0)
> 
> **参数:**
> 
> **buffer:**【buffer _ like】公开缓冲区接口的对象。
> 
> **数据类型:**【数据类型，可选】返回数组的数据类型，默认数据类型为 float。
> 
> **计数:**【int，可选】要读取的项目数。
> 
> **偏移量:**【int，可选】从此偏移量开始读取缓冲区，默认值为 0。
> 
> **返回:**这个函数将缓冲区解释为一维数组。

**代码#1 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.frombuffer() function 

# importing numpy as geek 
import numpy as geek

gfg = geek.frombuffer(b'\x01\x02\x03', dtype = geek.uint8)

print (gfg)
```

**输出:**

> [1 2 3]

**代码#2 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.frombuffer() function 

# importing numpy as geek 
import numpy as geek

gfg = geek.frombuffer(b'\x01\x02\x03\x04\x05\x06\x07', dtype = geek.uint8, count = 5)

print (gfg)
```

**输出:**

> [1 2 3 4 5]