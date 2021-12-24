# Python 中的 numpy.extract()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-extract-python/

**numpy.extract()** 函数返回 input_array 的元素，如果它们满足某个指定的条件。

```
Syntax: numpy.extract(condition, array)
```

**参数:**

```
array     : Input array. User apply conditions on input_array elements
condition : [array_like]Condition on the basis of which user extract elements. 
      Applying condition on input_array, if we print condition, it will return an array
      filled with either True or False. Array elements are extracted from the Indices having 
      True value.
```

**返回:**

```
Array elements that satisfy the condition.
```

## 计算机编程语言

```
# Python Program illustrating
# numpy.compress method

import numpy as geek

array = geek.arange(10).reshape(5, 2)
print("Original array : \n", array)

a = geek.mod(array, 4) !=0
# This will show element status of satisfying condition
print("\nArray Condition a : \n", a)

# This will return elements that satisfy condition "a" condition
print("\nElements that satisfy condition a  : \n", geek.extract(a, array))

b = array - 4 == 1
# This will show element status of satisfying condition
print("\nArray Condition b : \n", b)

# This will return elements that satisfy condition "b" condition
print("\nElements that satisfy condition b  : \n", geek.extract(b, array))
```

**输出:**

```
Original array : 
 [[0 1]
 [2 3]
 [4 5]
 [6 7]
 [8 9]]

Array Condition a : 
 [[False  True]
 [ True  True]
 [False  True]
 [ True  True]
 [False  True]]

Elements that satisfy condition a  : 
 [1 2 3 5 6 7 9]

Array Condition b : 
 [[False False]
 [False False]
 [False  True]
 [False False]
 [False False]]

Elements that satisfy condition b  : 
 [5]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . extract . html # numpy . extract](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.extract.html#numpy.extract)
**注意:**
同样，这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。