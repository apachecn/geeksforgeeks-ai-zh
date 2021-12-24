# 如何检查给定 NumPy 数组的元素是否非零？

> 原文:[https://www . geeksforgeeks . org/如何检查给定 numpy 数组的元素是否非零/](https://www.geeksforgeeks.org/how-to-check-whether-the-elements-of-a-given-numpy-array-is-non-zero/)

在 NumPy 中借助 **any()函数**，我们可以检查 NumPy 中给定数组的任意元素是否为非零。我们将在 any()函数中传递一个数组，如果它返回 true，那么该数组的任何元素都是非零的，如果它返回 false，那么该数组的所有元素都是零的。

> **语法:** numpy.any()
> 
> **参数**:数组。
> 
> **返回**:返回布尔值(真/假)。

**例 1:**

## 计算机编程语言

```py
import numpy as np

# Original array
array = np.array([4,6,0,0,0,4,89])
print(x)

# Test whether any of the elements
# of a given array is non-zero
print(np.any(array))
```

**输出:**

```py
True

```

**例 2:**

## 计算机编程语言

```py
import numpy as np

# Original array
array = np.array([0,0,0,0,0,0])
print(x)

# Test whether any of the elements
# of a given array is non-zero
print(np.any(array))
```

**输出:**

```py
False

```