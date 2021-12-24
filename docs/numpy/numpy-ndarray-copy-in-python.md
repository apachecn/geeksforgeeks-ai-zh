# python 中的 numpy . ndarray . copy()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-copy-in-python/

`**numpy.ndarray.copy()**`返回数组的副本。

> **语法:** numpy.ndarray.copy(顺序='C ')
> 
> **参数:**
> **顺序:**控制副本的内存布局。“C”表示 C 阶，“F”表示 F 阶，“A”表示“F”，如果 A 是 Fortran 连续的，则为“C”，否则为“C”。“k”表示尽可能匹配的布局。

**代码#1:**

```
# Python program explaining  
# numpy.ndarray.copy() function

import numpy as geek

x = geek.array([[0, 1, 2, 3], [4, 5, 6, 7]],
                                 order ='F')
print("x is: \n", x)

# copying x to y
y = x.copy()
print("y is :\n", y)
print("\nx is copied to y")
```

**Output:**

```
x is: 
 [[0 1 2 3]
 [4 5 6 7]]
y is :
 [[0 1 2 3]
 [4 5 6 7]]

x is copied to y

```

**代码#2:**

```
# Python program explaining  
# numpy.ndarray.copy() function

import numpy as geek

x = geek.array([[0, 1, ], [2, 3]])
print("x is:\n", x)

# copying x to y
y = x.copy()

# filling x with 1's
x.fill(1)
print("\n Now x is : \n", x)

print("\n y is: \n", y)
```

**Output:**

```
x is:
 [[0 1]
 [2 3]]

 Now x is : 
 [[1 1]
 [1 1]]

 y is: 
 [[0 1]
 [2 3]]

```