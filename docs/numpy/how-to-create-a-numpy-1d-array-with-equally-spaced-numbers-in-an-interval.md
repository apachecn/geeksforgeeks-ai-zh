# 如何创建一个区间内等间距数字的 NumPy 1D 阵列？

> 原文:[https://www . geeksforgeeks . org/如何创建等间距数字数组/](https://www.geeksforgeeks.org/how-to-create-a-numpy-1d-array-with-equally-spaced-numbers-in-an-interval/)

有时，我们需要制作不同类型的数组，如在 AP(等间距数列)、GP(指数间距数列)或 HP(等间距数列)中，以解决各种问题，特别是在解决一些科学或天文问题时，以减少计算量。就预实现代码而言，Python 是最好的语言之一，几乎每次都有，但代价是处理速度。

[NumPy](https://www.geeksforgeeks.org/python-numpy/) 有一个名为 [arange()](https://www.geeksforgeeks.org/numpy-arange-python/) [](https://numpy.org/doc/stable/reference/generated/numpy.arange.html)的内置方法，能够创建一个给定整数类型的数组(以字节为单位)，数字之间的间距相等。

> **语法:**保证([开始，]停止[，步骤，][，数据类型])
> 
> **参数:**
> 
> *   **开始:**这是默认参数。元素第一个数字的值，这个参数的默认值是 0。
> *   **停止:**这不是默认参数。这必须大于最后一个元素的最大可能值。例如，如果您希望最后一个元素是 8，则应该根据数组中两个连续数字之间的差异，将停止值设置为 9 或更大。
> *   **步骤:**这也是默认参数。这个数字将是数组中两个连续元素之间的差值。步骤的默认值是 1。
> *   **dtype:** 这也是默认参数。这是 NumPy 中数字的数据类型，为简单起见，它是一个前面有 np.int 的数字(2 的幂)，例如，np.int8，np.int16，np.int32。

该函数将根据用户的需求返回一个数组。让我们看看它的一些例子:

**示例 1:** 创建一个从 0 到给定数字的简单数组

## 蟒蛇 3

```
import numpy as np

# Here, the array has only one parameter,
# and that is the open ended limit of
# last number of the array
myArray = np.arange(8)
print(myArray)
```

**输出:**

```
[0 1 2 3 4 5 6 7]
```

**示例 2:** 创建一个从给定数字到另一个数字的简单数组

## 蟒蛇 3

```
import numpy as np

# This line has two parameters
# The first one is the closed and beginning limit
# The second one is the open and end limit
mySecondArray = np.arange(1, 6)
print(mySecondArray)
```

**输出:**

```
[1 2 3 4 5]
```

**示例 3:** 创建一个从给定数字到另一个具有给定间隔的数字的数组。

## 蟒蛇 3

```
import numpy as np

# This line has two parameters
# The first one is the closed and beginning limit
# The second one is the open and end limit
# The third one is the steps(difference between
# two  elements in the array)
myThirdArray = np.arange(2, 12, 2)
print(myThirdArray)
```

**输出:**

```
[ 2  4  6  8 10]
```

**示例 4:** 我们使用数据类型，尤其是在我们想要处理图像或某种其他计算的情况下。

## 蟒蛇 3

```
import numpy as np

# This line has two parameters
# The first one is the closed and beginning limit
# The second one is the open and end limit
# The third one is the steps(difference between
# two  elements in the array)
myForthArray = np.arange(5, 101, 10, np.int32)
print(myForthArray)
```

**输出:**

```
[ 5 15 25 35 45 55 65 75 85 95]
```