# 如何获取 numpy 数组元素的下限、上限和截断值？

> 原文:[https://www . geeksforgeeks . org/如何获取 numpy 数组元素的下限和上限截断值/](https://www.geeksforgeeks.org/how-to-get-the-floor-ceiling-and-truncated-values-of-the-elements-of-a-numpy-array/)

在本文中，让我们讨论如何获取 Numpy 数组元素的下限、上限和截断值。首先，我们需要导入 NumPy 库来使用其中所有可用的功能。这可以通过以下导入语句来完成:

```py
import numpy as np

```

### **获取楼层值**

小于或等于 x 的最大整数，其中 x 是数组元素，称为 floor 值。可以使用功能 [numpy.floor()](https://www.geeksforgeeks.org/numpy-floor-python/) 找到

**语法:**

```py
numpy.floor(x[, out]) = ufunc ‘floor’) 

```

**例 1:**

## 计算机编程语言

```py
# Import the numpy library
import numpy as np

# Initialize numpy array
a = np.array([1.2])

# Get floor value
a = np.floor(a)
print(a)
```

**输出:**

```py
[1.]

```

**例 2:**

## 计算机编程语言

```py
import numpy as np

a = np.array([-1.8, -1.6, -0.5, 0.5,
              1.6, 1.8, 3.0])

a = np.floor(a)
print(a)
```

**OutPut:**

```py
[-2., -2., -1., 0., 1., 1., 3.]

```

### **获取上限值**

大于或等于 x 的最小整数称为 ceil 值，其中 x 是数组元素。可以使用 [numpy.ceil()](https://www.geeksforgeeks.org/numpy-ceil-python/) 方法找到。

**语法:**

```py
numpy.ceil(x[, out]) = ufunc ‘ceil’) 

```

**例 1:**

## 计算机编程语言

```py
# Import the numpy library
import numpy as np

# Initialize numpy array
a = np.array([1.2])

# Get ceil value
a = np.ceil(a)
print(a)
```

**输出:**

```py
[2.]

```

**例 2:**

## 计算机编程语言

```py
import numpy as np

a = np.array([-1.8, -1.6, -0.5, 0.5,
              1.6, 1.8, 3.0])

a = np.ceil(a)
print(a)
```

**输出**:

```py
[-1., -1., -0., 1., 2., 2., 3.]

```

### **获取截断值**

标量 x 的中心是最接近的整数 I，比 x 更接近零。这简单地意味着，有符号数 x 的小数部分被这个函数丢弃。可以使用 [numpy.trunc()](https://www.geeksforgeeks.org/numpy-trunc-python/) 方法找到。

**语法:**

```py
numpy.trunc(x[, out]) = ufunc ‘trunc’)

```

**例 1:**

## 计算机编程语言

```py
# Import the numpy library
import numpy as np

# Initialize numpy array
a = np.array([1.2])

# Get truncate value
a = np.trunc(a)
print(a)
```

**输出:**

```py
[1.]

```

**例 2:**

## 计算机编程语言

```py
import numpy as np

a = np.array([-1.8, -1.6, -0.5, 0.5,
              1.6, 1.8, 3.0])

a = np.trunc(a)
print(a)
```

**输出:**

```py
[-1., -1., -0., 0., 1., 1., 3.]

```

**获取 numpy 数组元素的地板、天花板、躯干值的示例**

## 计算机编程语言

```py
import numpy as np

input_arr = np.array([-1.8, -1.6, -0.5, 0.5, 
                      1.6, 1.8, 3.0])
print(input_arr)

floor_values = np.floor(input_arr)
print("\nFloor values : \n", floor_values)

ceil_values = np.ceil(input_arr)
print("\nCeil values : \n", ceil_values)

trunc_values = np.trunc(input_arr)
print("\nTruncated values : \n", trunc_values)
```

**输出:**

```py
[-1.8 -1.6 -0.5  0.5  1.6  1.8  3\. ]

Floor values : 
 [-2\. -2\. -1\.  0\.  1\.  1\.  3.]

Ceil values : 
 [-1\. -1\. -0\.  1\.  2\.  2\.  3.]

Truncated values : 
 [-1\. -1\. -0\.  0\.  1\.  1\.  3.]

```