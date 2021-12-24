# 如何使用 Numpy 获得数组的元素级真除法？

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-get-element-wise-true-division-of-an-array-using-numpy/) 获取数组的逐元素真除法

**python 3 中的真除法**返回一个包含除法余数的浮点结果。为了得到数组的真除法，NumPy 库有一个函数 [**numpy.true_divide(x1，x2)**](https://www.geeksforgeeks.org/numpy-true_divide-python/) 。这个函数给出了传递给函数的数组的真除法的值。为了得到元素分割，我们需要输入第一个参数作为数组，第二个参数作为单个元素。

> **语法:** np.true_divide(x1，x2)
> **参数:**
> 
> *   **x1: T** he 红利阵
> *   **x2:** 除数(可以是数组或元素)
> 
> **返回:**如果输入是标量，那么是标量；否则用 arr1 / arr2(元素方式)排列，即真除法

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create 1d-array
x = np.arange(5)

print("Original array:", 
      x)

# apply true division 
# on each array element
rslt = np.true_divide(x, 4)

print("After the element-wise division:", 
      rslt)
```

**输出**T2:

```py
Original array: [0 1 2 3 4]
After the element-wise division: [0\.   0.25 0.5  0.75 1\.  ]
```

**例 2:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a 1d-array
x = np.arange(10)

print("Original array:", 
      x)

# apply true division 
# on each array element
rslt = np.true_divide(x, 3)

print("After the element-wise division:",
      rslt)
```

**输出:**

> 原始数组:[0 1 2 3 4 5 6 7 8 9]
> 元素分割后:[0。0.33333333 0.66666667 1.1.33333333 1.6666667
> 2。2.33333333 2.66666667 3.]