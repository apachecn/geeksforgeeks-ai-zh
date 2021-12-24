# numpy.fromstring()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-from string-function-python/](https://www.geeksforgeeks.org/numpy-fromstring-function-python/)

函数的作用是:从字符串中的文本数据创建一个新的一维数组。

> **语法:** numpy.fromstring(字符串，dtype = float，count = -1，sep = ' ')
> 
>  **参数:
> 
> 字符串:[字符串]包含数据的字符串。
> 
> 数据类型:[数据类型，可选]数组的数据类型。默认数据类型是浮点型。
> 
> 计数:[int，可选]要读取的项目数。如果为负(默认值)，计数将根据数据的长度来确定。
> 
> sep:[字符串，可选]分隔数据中数字的字符串。
> 
> 返回:[ndarray]返回构造的数组。**

**代码#1:**

## **蟒蛇 3**

```
# Python program explaining
# numpy.fromstring() function

# importing numpy as geek
import numpy as geek

gfg = geek.fromstring('1 2 3 4 5', dtype = float, sep = ' ')

print(gfg)
```

**输出:**

> **[1\. 2\. 3\. 4\. 5.]**

**代码#2:**

## **蟒蛇 3**

```
# Python program explaining
# numpy.fromstring() function

# importing numpy as geek
import numpy as geek

gfg = geek.fromstring('1 2 3 4 5 6', dtype = int, sep = ' ')

print(gfg)
```

**输出:**

> **[1 2 3 4 5 6]**