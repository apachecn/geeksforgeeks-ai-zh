# 如何使用给定的索引位置重新排列 2D NumPy 数组的列？

> 原文:[https://www . geeksforgeeks . org/如何使用给定的索引位置重新排列 2d numpy 数组的列/](https://www.geeksforgeeks.org/how-to-rearrange-columns-of-a-2d-numpy-array-using-given-index-positions/)

在本文中，我们将学习如何使用给定的索引位置重新排列给定的 [numpy 数组](https://www.geeksforgeeks.org/python-numpy/#:~:text=Array%20in%20Numpy%20is%20a,a%20tuple%20of%20positive%20integers.&text=An%20array%20class%20in%20Numpy,by%20using%20nested%20Python%20Lists.)的列。这里，列根据给定的索引重新排列。为此，我们可以简单地将列值存储在列表中，并根据给定的索引列表排列这些值，但是这种方法非常昂贵。因此，通过使用 numpy 数组的概念，这可以很容易地在最短的时间内完成。

#### 示例:

> Arr = [[1，2，3，4，5]，[1，2，3，4，5]，[1，2，3，4，5]，[1，2，3，4，5]]和 i = [2，4，0，3，1]
> 则输出为[[3，5，1，4，2]，[3，5，1，4，2]，[3，5，1，4，2]，[3，5，1，4，2]，[3，5，1，4，2]，[3，5，1，2]
> 
> 这里，i[0] = 2 即；第三列 so 输出= [[3]，[3]，[3]，][3]，[3]]。
> i[1] = 4 即；第 5 列 so 输出= [[3，5]，[3，5]，[3，5]，][3，5]，[3，5]]。
> i[2] = 0 即；第一列 so 输出= [[3，5，1]，[3，5，1]，[3，5，1]，][3，5，1]，[3，5，1]]。
> i[3] = 3 即；第 4 列 so 输出= [[3，5，1，4]，[3，5，1，4]，[3，5，1，4]，][3，5，1，4]，[3，5，1，4]]。
> i[4] = 1 即；第二列 so 输出= [[3，5，1，4，2]，[3，5，1，4，2]，[3，5，1，4，2]，][3，5，1，4，2]，[3，5，1，4，2]]。

下面是一个示例的实现:

## 蟒蛇 3

```
# importing package
import numpy

# create a numpy array
arr = numpy.array([[1,2,3,4,5],
                   [1,2,3,4,5],
                   [1,2,3,4,5],
                   [1,2,3,4,5],
                   [1,2,3,4,5]
                   ])

# view array
print(arr)

# declare index list
i = [2,4,0,3,1]

# create output
output = arr[:,i]

# view output
print(output)
```

**输出:**

```
[[1 2 3 4 5]
 [1 2 3 4 5]
 [1 2 3 4 5]
 [1 2 3 4 5]
 [1 2 3 4 5]]
[[3 5 1 4 2]
 [3 5 1 4 2]
 [3 5 1 4 2]
 [3 5 1 4 2]
 [3 5 1 4 2]]

```