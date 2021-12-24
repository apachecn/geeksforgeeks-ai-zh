# python 中的 numpy . ndarray . fill()

> 原文:[https://www.geeksforgeeks.org/numpy-ndarray-fill-in-python/](https://www.geeksforgeeks.org/numpy-ndarray-fill-in-python/)

numpy.ndarray.fill()方法用于用标量值填充 numpy 数组。

如果我们必须用相同的值初始化 numpy 数组，那么我们使用 numpy.ndarray.fill()。假设我们必须创建一个长度为 n 的 NumPy 数组 *a* ，其中每个元素都是 v。然后我们使用这个函数作为 a.fill(v)。如果我们使用这个`fill()`函数，我们不需要使用循环来初始化数组。

> **语法** : ndarray.fill(值)
> 
> **参数:**
> **值:**一个的所有元素都会被赋予这个值。

**代码#1:**

```py
# Python program explaining
# numpy.ndarray.fill() function
import numpy as geek

a = geek.empty([3, 3])

# Initializing each element of the array
# with 1 by using nested loops 
for i in range(3):
    for j in range(3):
        a[i][j] = 1

print("a is : \n", a)    

# now we are initializing each element
# of the array with 1 using fill() function. 
a.fill(1)

print("\nAfter using fill() a is : \n", a)

```

**Output:**

```py
a is : 
 [[ 1\.  1\.  1.]
 [ 1\.  1\.  1.]
 [ 1\.  1\.  1.]]

After using fill() a is : 
 [[ 1\.  1\.  1.]
 [ 1\.  1\.  1.]
 [ 1\.  1\.  1.]]

```

**代码#2:**

```py
# Python program explaining
# numpy.ndarray.fill() function
import numpy as geek

a = geek.arange(5)

print("a is \n", a)

# Using fill() method
a.fill(0)

print("\nNow a is :\n", a)

```

**Output:**

```py
a is 
 [0 1 2 3 4]

Now a is :
 [0 0 0 0 0]

```

**代码#3:** numpy.ndarray.fill()也适用于多维数组。

```py
# Python program explaining
# numpy.ndarray.fill() function

import numpy as geek

a = geek.empty([3, 3])

# Using fill() method
a.fill(0)

print("a is :\n", a)
```

**Output:**

```py
a is :
 [[ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]]

```