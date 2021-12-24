# Numpy 字符串操作| startswith()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-starts with-function/](https://www.geeksforgeeks.org/numpy-string-operations-startswith-function/)

numpy . core . defchararray . start swith()函数返回一个布尔数组，如果中的字符串元素以前缀开头，则返回 True，否则返回 False。

> **语法:**num py . core . defchararray . start with(arr，prefix，start = 0，end = None)
> 
> **参数:**
> 
> **arr :** 【字符串数组或 unicode】字符串数组。
> 
> **前缀:**【字符串】输入字符串。
> 
> **开始，结束:**【int，可选】可选开始，测试从该位置开始。可选结束，停止在该位置比较。
> 
> **返回:**【ndarray】返回布尔数组。

**代码#1 :**

## 蟒蛇 3

```
# Python program explaining 
# numpy.char.startswith() function 

# importing numpy as geek  
import numpy as geek 

arr = "GeeksforGeeks - A computer science portal"
prefix = 'Geeks'

gfg = geek.char.startswith(arr, prefix, start = 0, end = None)

print (gfg)
```

**输出:**

> 真实的

**代码#2 :**

## 蟒蛇 3

```
# Python program explaining 
# numpy.char.startswith() function 

# importing numpy as geek  
import numpy as geek 

arr = "GeeksforGeeks - A computer science portal"
prefix = 'None'

gfg = geek.char.startswith(arr, prefix, start = 0, end = None)

print (gfg)
```

**输出:**

> 错误的