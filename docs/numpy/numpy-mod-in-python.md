# python 中的 numpy.mod()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-mod-in-python/

**`numpy.mod()`** 是 numpy 中做数学运算的另一个函数。它返回两个数组 arr1 和 arr2(即`arr1 % arr2` )之间的按元素划分的余数。当 arr2 为 0 并且 arr1 和 arr2 都是整数(数组)时，它返回 0。

> **语法:** numpy.mod(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc '余数')
> 
> **参数:**
> **arr1 :** 【阵 _ 象】红利阵。
> **arr 2:**【array _ like】除数数组。
> **dtype :** 返回数组的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **返回:**【ndarray】元素方向的余数，即 arr1 % arr2。

**代码#1 :**

```
# Python program explaining
# numpy.mod() function

import numpy as geek
in_num1 = 6
in_num2 = 4

print ("Dividend : ", in_num1)
print ("Divisor : ", in_num2)

out_num = geek.mod(in_num1, in_num2) 
print ("Remainder : ", out_num) 
```

**Output :**

```
Dividend :  6
Divisor :  4
Remainder :  2

```

**代码#2 :**

```
# Python program explaining
# numpy.mod() function

import numpy as geek

in_arr1 = geek.array([2, -4, 7])
in_arr2 = geek.array([2, 3, 4])

print ("Dividend array : ", in_arr1)
print ("Divisor array : ", in_arr2)

out_arr = geek.mod(in_arr1, in_arr2) 
print ("Output remainder array: ", out_arr) 
```

**Output :**

```
Dividend array :  [ 2 -4  7]
Divisor array :  [2 3 4]
Output remainder array:  [0 2 3]

```