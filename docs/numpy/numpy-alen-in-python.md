# python 中的 numpy.alen()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-alen-in-python/

**`numpy.alen()`** 函数用于返回输入数组的第一维的长度。

> **语法:** numpy.alen(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【int】arr 第一维的长度。

**代码#1 :**

```
# Python program explaining
# alen() function

import numpy as geek

# input array(2 * 3)
in_arr = geek.array([[ 2, 0, 7], [ 0, 5, 9]])
print ("Input array : ", in_arr) 

out_dim = geek.alen(in_arr)
print ("Length of the first dimension of arr: ", out_dim)
```

**Output:**

```
Input array :  [[2, 0, 7], [0, 5, 9]]
Length of the first dimension of arr:  2

```

**代码#2 :**

```
# Python program explaining
# alen() function

import numpy as geek

# input array(1 * 3*3)
in_arr = geek.arange(9).reshape(1, 3, 3)
print ("Input array : \n", in_arr) 

out_dim = geek.alen(in_arr)
print ("Length of the first dimension of arr: ", out_dim)
```

**Output:**

```
Input array : 
 [[[0 1 2]
  [3 4 5]
  [6 7 8]]]
Length of the first dimension of arr:  1

```