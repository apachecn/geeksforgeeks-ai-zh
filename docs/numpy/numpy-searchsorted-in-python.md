# Python 中的 numpy.searchsorted()

> 原文:[https://www.geeksforgeeks.org/numpy-searchsorted-in-python/](https://www.geeksforgeeks.org/numpy-searchsorted-in-python/)

**`numpy.searchsorted()`** 函数用于将索引查找到排序数组 arr 中，这样，如果在索引之前插入元素，arr 的顺序仍会保留。这里，二分搜索法被用来寻找所需的插入指数。

> **语法:** numpy.searchsorted(arr，num，side='left '，sorter=None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。如果排序器为无，则必须按升序排序，否则排序器必须是对其排序的索引数组。
> **编号:**【类似数组】我们要插入 arr 的值。
> **侧:** ['左'，'右']，可选。如果“左”，则给出找到的第一个合适位置的索引。如果“正确”，返回最后一个这样的索引。如果没有合适的索引，返回 0 或 N(其中 N 是 a 的长度)。
> **num:**【array _ like，Optional】将数组 a 按升序排序的整数索引数组。它们通常是 argsort 的结果。
> 
> **返回:**【索引】，与 num 形状相同的插入点数组。

**代码#1:工作**

```py
# Python program explaining
# searchsorted() function

import numpy as geek

# input array
in_arr = [2, 3, 4, 5, 6]
print ("Input array : ", in_arr)

# the number which we want to insert
num = 4
print("The number which we want to insert : ", num) 

out_ind = geek.searchsorted(in_arr, num) 
print ("Output indices to maintain sorted array : ", out_ind)
```

**输出:**

```py
Input array :  [2, 3, 4, 5, 6]
The number which we want to insert :  4
Output indices to maintain sorted array :  2

```

**代码#2 :**

```py
# Python program explaining
# searchsorted() function

import numpy as geek

# input array
in_arr = [2, 3, 4, 5, 6]
print ("Input array : ", in_arr)

# the number which we want to insert
num = 4
print("The number which we want to insert : ", num)   

out_ind = geek.searchsorted(in_arr, num, side ='right') 
print ("Output indices to maintain sorted array : ", out_ind)
```

**输出:**

```py
Input array :  [2, 3, 4, 5, 6]
The number which we want to insert :  4
Output indices to maintain sorted array :  3

```

**代码#3 :**

```py
# Python program explaining
# searchsorted() function

import numpy as geek

# input array
in_arr = [2, 3, 4, 5, 6]
print ("Input array : ", in_arr)

# the numbers which we want to insert
num = [4, 8, 0]
print("The number which we want to insert : ", num)   

out_ind = geek.searchsorted(in_arr, num) 
print ("Output indices to maintain sorted array : ", out_ind)
```

**输出:**

```py
Input array :  [2, 3, 4, 5, 6]
The number which we want to insert :  [4, 8, 0]
Output indices to maintain sorted array :  [2 5 0]

```