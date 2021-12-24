# 在 NumPy 中创建自己的通用函数

> 原文:[https://www . geesforgeks . org/create-your-your-your-universal-function-in-numpy/](https://www.geeksforgeeks.org/create-your-own-universal-function-in-numpy/)

[**Numpy 中的通用函数**](https://www.geeksforgeeks.org/numpy-ufunc-universal-functions/) 都是简单的数学函数。这只是我们在 Numpy 库中赋予数学函数的一个术语。Numpy 提供各种通用功能，涵盖各种操作。但是，我们可以在 Python 中创建自己的通用函数。要在 NumPy 中创建自己的通用函数，我们必须应用下面给出的一些步骤:

1.  通常使用 def 关键字定义。
2.  使用 frompyfunc()方法将此函数添加到 numpy 库中。
3.  使用 numpy 使用此功能。

## frompyfunc()方法

这个函数允许创建一个任意的 Python 函数作为 Numpy ufunc(通用函数)。此方法采用以下参数:

> **参数:**
> 
> *   **函数**–您创建的函数的名称。
> *   **输入**–函数采用的输入参数(数组)数量。
> *   **输出**–函数产生的输出(数组)数量。

**注意:**更多信息请参考 Python 中的 [numpy.frompyfunc()。](https://www.geeksforgeeks.org/numpy-frompyfunc-in-python/)

**示例:**

*   创建一个名为 fxn 的函数，该函数接受一个值并返回一个值。
*   输入是一个接一个的数组元素。
*   输出是使用一些逻辑修改的数组元素。

## 蟒蛇 3

```py
# using numpy
import numpy as np

# creating own function
def fxn(val):
  return (val % 2)

# adding into numpy
mod_2 = np.frompyfunc(fxn, 1, 1)

# creating numpy array
arr = np.arange(1, 11)
print("arr     :", *arr)

# using function over numpy array
mod_arr = mod_2(arr)
print("mod_arr :", *mod_arr)
```

**输出:**

```py
arr     : 1 2 3 4 5 6 7 8 9 10
mod_arr : 1 0 1 0 1 0 1 0 1 0
```