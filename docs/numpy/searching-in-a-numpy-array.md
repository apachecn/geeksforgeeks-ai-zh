# 在 NumPy 数组中搜索

> 原文:[https://www.geeksforgeeks.org/searching-in-a-numpy-array/](https://www.geeksforgeeks.org/searching-in-a-numpy-array/)

Numpy 提供了各种方法来搜索不同种类的数值，在本文中，我们将介绍两种重要的方法。

*   **numpy.where()**
*   **numpy.searchsorted()**

**1。numpy.where:()** 它返回满足给定条件的输入数组中元素的索引。

> **语法:** numpy.where(条件[，x，y])
> 
> ***参数:***
> 
> *   ***条件:**为真时，收益率为 x，否则收益率为 y。*
> *   ***x，y :** 可供选择的数值。x、y 和条件需要可以扩展到某种形状。*
> 
> ***返回:***
> ***out:**【n 数组或 n 数组的元组】如果同时指定了 x 和 y，则输出数组包含 x 的元素，其中条件为真，其他地方包含 y 的元素。*
> 
> *如果只给定条件，返回元组条件非零()，条件为真的索引。*

以下示例演示了如何使用 *where()* 进行搜索。

## 蟒蛇 3

```
# importing the module
import numpy as np

# creating the array
arr = np.array([10, 32, 30, 50, 20, 82, 91, 45])

#  printing arr
print("arr = {}".format(arr))

#  looking for value 30 in arr and storing its index in i
i = np.where(arr == 30)
print("i = {}".format(i))
```

**输出:**

```
arr = [10 32 30 50 20 82 91 45]
i = (array([2], dtype=int64),)

```

如您所见，变量 I 是一个可迭代的变量，我们搜索的值的索引是第一个元素。我们可以通过将最后一个 print 语句替换为

```
print("i = {}".format(i[0]))

```

这会将最终输出更改为

```
arr = [10 32 30 50 20 82 91 45]
i = [2]

```

**2。numpy.searchsorted():** 该函数用于查找排序数组 arr 中的索引，这样，如果在索引之前插入元素，arr 的顺序仍将保持不变。这里，使用二分搜索法来找到所需的插入索引。

> ***语法:** numpy.searchsorted(arr，num，side='left '，sorter=None)*
> 
> ***参数:***
> 
> *   ***arr :** 【类阵】输入阵。如果排序器为无，则必须按升序排序，否则排序器必须是对其排序的索引数组。*
> *   ***num:**【array _ like】我们要插入 arr 的值。*
> *   ***侧:** ['左'，'右']，可选。如果“左”，则给出找到的第一个合适位置的索引。如果“正确”，返回最后一个这样的索引。如果没有合适的索引，返回 0 或 N(其中 N 是 a 的长度)。*
> *   ***num:**【array _ like，Optional】将数组 a 按升序排序的整数索引数组。它们通常是 argsort 的结果。*
> 
> ***返回:**【索引】，与 num 形状相同的插入点数组。*

下面的例子解释了 *searchsorted()* 的用法。

## 蟒蛇 3

```
# importing the module
import numpy as np

# creating the array
arr = [1, 2, 2, 3, 3, 3, 4, 5, 6, 6]
print("arr = {}".format(arr))

# left-most 3
print("left-most index = {}".format(np.searchsorted(arr, 3, side="left")))

# right-most 3
print("right-most index = {}".format(np.searchsorted(arr, 3, side="right")))
```

**输出:**

```
arr = [1, 2, 2, 3, 3, 3, 4, 5, 6, 6]
left-most index = 3
right-most index = 6

```