# 计算 NumPy 数组中非 NaN 元素的数量

> 原文:[https://www . geeksforgeeks . org/counting-numpy 数组中非 nan 元素的数量/](https://www.geeksforgeeks.org/counting-the-number-of-non-nan-elements-in-a-numpy-array/)

在本文中，我们将看到如何在 Python 中计算 NumPy 数组中非 NaN 元素的数量。

**NAN:** 当你不在乎那个位置的值是多少时使用。也许有时是用来代替丢失的数据或损坏的数据。

## 方法 1:使用条件

在这个例子中，我们将使用一维数组。在下面给出的代码中，我们遍历给定 NumPy 数组的每个条目，并检查该值是否是 NaN。

## 蟒蛇 3

```
import numpy as np

ex1 = np.array([1, 4, -9, np.nan])
ex2 = np.array([1, 45, -2, np.nan, 3, 
                -np.nan, 3, np.nan])

def approach_1(data):
    # here the input data, is a numpy ndarray

    # initialize the number of non-NaN elements 
    # in data
    count = 0       

    # loop over each entry of the data
    for entry in data:          

          # check whether the entry is a non-NaN value
        # or not
        if not np.isnan(entry):     

              # if not NaN, increment "count" by 1
            count += 1              
    return count

print(approach_1(ex1))
print(approach_1(ex2))
```

**输出:**

```
3
5
```

## 方法二:使用 [isnan()](https://www.geeksforgeeks.org/numpy-isnan-python/)

利用 NumPy 数组的功能，我们可以一次对整个数组而不是单个元素执行操作。

**已用功能:**

*   np.isnan(数据):对数组的条目执行 np.isnan()操作后返回一个布尔数组，数据
*   np.sum():因为我们正在向 sum 函数输入一个布尔数组，所以它返回 bool 数组中 True 值(1s)的数量。

## 蟒蛇 3

```
import numpy as np

ex3 = np.array([[3, 4, -390, np.nan], 
                [np.nan, np.nan, np.nan, -90]])

def approach_2(data):
    return np.sum(~np.isnan(data))

print(approach_2(ex3))
```

**输出:**

```
4
```

## 方法三:使用[**NP . count _ 非零()**功能](https://www.geeksforgeeks.org/numpy-count_nonzero-method-python/)

**numpy . count _ 非零()**函数计算数组 arr 中非零值的个数。

> **语法:**numpy . count _ 非零(arr，axis =无)
> 
> **参数:**
> **arr:**【array _ like】要计算非 0 的数组。
> **轴:**【int 或 tuple，可选】轴或轴的 tuple，沿其计数非 0。默认值为“无”，这意味着非 0 将沿着平坦版本的 arr 进行计数。
> 
> **返回:**【int 或 int 数组】数组中沿给定轴的非零值的数量。否则，返回数组中非零值的总数。

## 蟒蛇 3

```
import numpy as np

ex4 = np.array([[0.35834379, 0.67202438, np.nan, np.nan,
                 np.nan, 0.47870971],
                [np.nan, np.nan, np.nan, 0.08113384,
                 0.70511741, 0.15260996],
                [0.09028477, np.nan, 0.16639899,
                    0.47740582, 0.7259116,  0.94797347],
                [0.80305651,     np.nan, 0.67949724,
                    0.84112054, 0.15951702, 0.07510587],
                [0.28643337, 0.00804256, 0.36775056,
                 0.19360266, 0.07288145, 0.37076932]])

def approach_3(data):
    return data.size - np.count_nonzero(np.isnan(data))

print(approach_3(ex4))
```

**输出:**

```
22
```