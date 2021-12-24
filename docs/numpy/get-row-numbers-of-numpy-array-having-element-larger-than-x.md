# 获取元素大于 X 的 NumPy 数组的行号

> 原文:[https://www . geeksforgeeks . org/get-row-numpy-array-having-element-big-x/](https://www.geeksforgeeks.org/get-row-numbers-of-numpy-array-having-element-larger-than-x/)

让我们看看如何获取至少有一个项目大于指定值 x 的 [numpy 数组](https://www.geeksforgeeks.org/python-numpy/#:~:text=Array%20in%20Numpy%20is%20a,a%20tuple%20of%20positive%20integers.&text=An%20array%20class%20in%20Numpy,by%20using%20nested%20Python%20Lists.)的行号。因此，为了完成此任务，我们将一起使用 [numpy.where()](https://www.geeksforgeeks.org/numpy-where-in-python/) 和 [numpy.any()](https://www.geeksforgeeks.org/numpy-any-in-python/) 函数。

> **语法:** numpy.where(条件[，x，y])
> 
> **Return:**【n 数组或 n 数组的元组】如果同时指定了 x 和 y，则输出数组包含 x 的元素，其中条件为 True，其他地方包含 y 的元素。
> 
> **语法:** numpy.any(a，axis = None，out = None，keepdims = class numpy。_ 全局。_NoValue 在 0x40ba726c)
> 
> **返回:**【n 数组，可选】输出数组与输入数组具有相同的维数，与结果一起放置

**示例:**

```
Arr = [[1,2,3,4,5], 
      [10,-3,30,4,5], 
      [3,2,5,-4,5], 
      [9,7,3,6,5]] 
and X = 6 then output is [ 0, 2 ].

Here, 
[[1,2,3,4,5],
no element is greater than 6 so output is [0].

[10,-3,30,4,5],
10 is greater than 6 so output is [0].

[3,2,5,-4,5],
no element is greater than 6 so output is [0, 2].

[4,7,3,6,5]]
7 is greater than 6 so output is [0, 2].

```

下面是实现:

## 蟒蛇 3

```
# importing library
import numpy

# create numpy array
arr = numpy.array([[1, 2, 3, 4, 5],
                  [10, -3, 30, 4, 5],
                  [3, 2, 5, -4, 5],
                  [9, 7, 3, 6, 5] 
                 ])

# declare specified value
X = 6

# view array
print("Given Array:\n", arr)

# finding out the row numbers
output  = numpy.where(numpy.any(arr > X,
                                axis = 1))

# view output
print("Result:\n", output)
```

**输出:**

```
Given Array:
[[ 1  2  3  4  5]
[10 -3 30  4  5]
[ 3  2  5 -4  5]
[ 9  7  3  6  5]]
Result:
(array([1, 3], dtype=int64),)

```