# 如何求 NumPy 1d-array 中的最大值和最小值？

> 原文:[https://www . geeksforgeeks . org/如何找到 numpy-1d-array 中的最大值和最小值/](https://www.geeksforgeeks.org/how-to-find-the-maximum-and-minimum-value-in-numpy-1d-array/)

让我们看看在 NumPy 1d-array 中找到最大值和最小值的各种方法。

**方法一:**利用 numpy 库的[**【NumPy . amax()】**](https://www.geeksforgeeks.org/numpy-amax-python/)[**NumPy . Amin()**](https://www.geeksforgeeks.org/numpy-amin-python/)功能。

*   **numpy.amax():** 此函数返回数组的最大值或沿轴的最大值(如有提及)。
*   **numpy.amin():** 此函数返回数组的最小值或沿轴的最小值(如果提到的话)。

**示例:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 1d-array
array = np.array([1, 2, 3, 
                  0, -1, -2])

# find max element in an array
max_ele = np.amax(array)

# find man element in an array
min_ele = np.amin(array)

# show the outputs
print("Given Array:", array)

print("Max Element:", max_ele)

print("Min Element:", min_ele)
```

**输出:**

```py
Given Array: [ 1  2  3  0 -1 -2]
Max Element: 3
Min Element: -2

```

**方法二:**利用 numpy 库的[**【NumPy . argmax()】**](https://www.geeksforgeeks.org/numpy-argmax-python/)[**NumPy . argmin()**](https://www.geeksforgeeks.org/numpy-argmin-python/)功能。

*   **numpy.argmax():** 此函数返回数组中最大元素在特定轴上的索引(如果提到的话)。
*   **numpy.argmin():** 该函数返回特定轴上数组的 min 元素的索引(如果提到的话)。

**示例:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 1d-array
array = np.array([1, 2, 3,
                  0, -1, -2])

# find index of max element
# in an array
max_ele_index = np.argmax(array)

# find max element in an array
max_ele = array[max_ele_index]

# find index of min element
# in an array
min_ele_index = np.argmin(array)

# find min element in an array
min_ele = array[min_ele_index]

# show the outputs
print("Given Array:", array)

print("Max Element:", max_ele)

print("Min Element:", min_ele)
```

**输出:**

```py
Given Array: [ 1  2  3  0 -1 -2]
Max Element: 3
Min Element: -2

```