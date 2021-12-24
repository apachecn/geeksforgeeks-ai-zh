# 使用 NumPy

以浮点精度计算 1 加每个元素的自然对数

> 原文:[https://www . geeksforgeeks . org/使用-numpy/](https://www.geeksforgeeks.org/compute-the-natural-logarithm-of-one-plus-each-element-in-floating-point-accuracy-using-numpy/) 计算浮点精度中每个元素的自然对数

让我们看看使用 NumPy 库以浮点精度计算给定数组的每个元素加 1 的自然对数的程序。

为了完成这个任务，我们使用了 numpy 的 [**numpy.log1p()**](https://www.geeksforgeeks.org/numpy-log1p-python/) 功能。这个函数返回一个自然对数的数组加上输入数组的每个元素。

> **语法:** numpy.log1p(arr，out = None，*其中= True，casting = 'same_kind '，order = 'K '，dtype = None，ufunc 'log1p ')

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```py
# Import numpy library
import numpy as np

# Create a numpy array
arr = np.array([1e-90, 1e-100])

# Applying the function
rslt = np.log1p(arr)

print(rslt)
```

**输出:**

```py
[1.e-090 1.e-100]
```

**例 2:**

## 蟒蛇 3

```py
# Import numpy library
import numpy as np

# Create a numpy array
arr = np.array([1, 2, 3, 4])

# Applying the function
rslt = np.log1p(arr)

print(rslt)
```

**输出:**

```py
[0.69314718 1.09861229 1.38629436 1.60943791]
```

**例 3:**

## 蟒蛇 3

```py
# Import numpy library
import numpy as np

# Create a numpy array
arr = np.array([1, 1e-1, 3, 1e-0])

# Applying the function
rslt = np.log1p(arr)

print(rslt)
```

**输出:**

```py
[0.69314718 0.09531018 1.38629436 0.69314718]
```