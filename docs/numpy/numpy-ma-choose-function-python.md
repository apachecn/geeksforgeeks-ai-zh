# numpy.ma.choose()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-ma-choose-function-python/](https://www.geeksforgeeks.org/numpy-ma-choose-function-python/)

**`numpy.ma.choose()`** 函数使用一个索引数组从一组选择中构造一个新数组。给定一个整数数组和一组 n 个选择数组，这个方法将创建一个新的数组来合并每个选择数组。当 arr 中的 arr 值为 I 时，新数组的值将与 choice[I]包含的值相同。

> **语法:** numpy.ma.choose(arr，choices，out = None，mode = 'raise ')
> 
> **参数:**
> **arr :** 【整数数组】该数组必须包含[0，n-1]中的整数，其中 n 为选择数。
> **选择:**【数组序列】选择数组。索引数组和所有选项应该可以扩展到相同的形状。
> **出:**【数组，可选】如果提供，结果会插入到这个数组中。它应该是适当的形状和数据类型。
> **模式:** [{ '提升'，'环绕'，'剪辑' }，可选]指定越界索引的行为方式。'引发':引发错误。“环绕”:环绕。'剪辑':剪辑到该范围。
> 
> **返回:**合并每个选择数组的新数组。

**代码#1 :**

```
# Python program explaining
# numpy.ma.choose() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

choice = geek.array([[1, 1, 1], [2, 2, 2], [3, 3, 3]])
arr = geek.array([2, 1, 0])

gfg = geek.ma.choose(arr, choice)

print (gfg)
```

**输出:**

```
[3 2 1]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.choose() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

choice = geek.array([[1, 1, 1], [2, 2, 2], [3, 3, 3]])
arr = geek.array([0, 1, 2])

gfg = geek.ma.choose(arr, choice)

print (gfg)
```

**输出:**

```
[1 2 3]

```