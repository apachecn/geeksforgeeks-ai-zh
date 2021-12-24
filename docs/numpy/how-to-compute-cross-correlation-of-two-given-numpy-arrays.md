# 如何计算两个给定 NumPy 阵列的互相关？

> 原文:[https://www . geeksforgeeks . org/如何计算两个给定 numpy 数组的互相关/](https://www.geeksforgeeks.org/how-to-compute-cross-correlation-of-two-given-numpy-arrays/)

在 Numpy 程序中，我们可以借助相关()计算两个给定数组的互相关。在第一个参数和第二个参数传递给给定数组时，它将返回两个给定数组的互相关。

> ***语法:** numpy.correlate(a，v，mode = 'valid')*
> 
> ***参数:***
> ***a、v:**【array _ like】输入序列。*
> ***模式:**【{ '有效'，'相同'，'完整' }，可选】参考卷积文档字符串。默认值为“有效”。*
> 
> ***返回:**【ndarray】a 与 v 的离散互相关*

**例 1:**

在本例中，我们将创建两个 NumPy 数组，任务是使用 ***关联()*** 计算互相关。

## 蟒蛇 3

```py
import numpy as np
array1 = np.array([0, 1, 2])
array2 = np.array([3, 4, 5])

# Original array1
print(array1)

# Original array2
print(array2)

# ross-correlation of the arrays
print("\nCross-correlation:\n",
      np.correlate(array1, array2))
```

**输出:**

```py
[0 1 2]
[3 4 5]

Cross-correlation:
 [14]
```

**例**T2【2:

## 蟒蛇 3

```py
import numpy as np
array1 = np.array([1,2])
array2 = np.array([1,2])

# Original array1
print(array1)

# Original array2
print(array2)
# Cross-correlation of the arrays
print("\nCross-correlation:\n",
      np.correlate(array1, array2))
```

**输出:**

```py
[1 2]
[1 2]

Cross-correlation:
 [5]
```