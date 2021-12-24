# num py ndaarray . item set()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-item set-function-python/

**`numpy.ndarray.itemset()`** 函数将标量插入数组。
至少要有 1 个参数，最后一个参数定义为 item。那么，arr.itemset(*args)相当于 arr[args] = item，但比 arr[args]= item 快。该项应该是标量值，参数必须在数组 arr 中选择一项。

> **语法:**num py . ndaarray . item set(* args)
> 
> **参数:**
> ***参数:**如果一个参数:标量，仅在 arr 大小为 1 的情况下使用。如果有两个参数:最后一个参数是要设置的值，并且必须是标量，则第一个参数指定单个数组元素的位置。它要么是一个 int，要么是一个元组。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.itemset() function

# importing numpy as geek 
import numpy as geek

geek.random.seed(345)
arr = geek.random.randint(9, size =(3, 3))
print("Input array : ", arr)

arr.itemset(4, 0)

print ("Output array : ", arr)
```

**输出:**

```
Input array :  [[8 0 3]
 [8 4 3]
 [4 1 7]]
Output array :  [[8 0 3]
 [8 0 3]
 [4 1 7]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.itemset() function

# importing numpy as geek 
import numpy as geek

geek.random.seed(345)
arr = geek.random.randint(9, size =(3, 3))
print("Input array : ", arr)

arr.itemset((2, 2), 9)

print ("Output array : ", arr)
```

**输出:**

```
Input array :  [[8 0 3]
 [8 4 3]
 [4 1 7]]
Output array :  [[8 0 3]
 [8 4 3]
 [4 1 9]]

```