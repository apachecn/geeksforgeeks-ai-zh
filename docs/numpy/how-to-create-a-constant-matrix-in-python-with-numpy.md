# 如何用 NumPy 在 Python 中创建常数矩阵？

> 原文:[https://www . geeksforgeeks . org/如何用 numpy 创建 python 中的常数矩阵/](https://www.geeksforgeeks.org/how-to-create-a-constant-matrix-in-python-with-numpy/)

一个**矩阵**代表一个按照行和列的顺序排列的数字集合。有必要用圆括号或括号把矩阵的元素括起来。**常数矩阵**是一种元素相同的矩阵，即元素不随任何索引值而变化，因此充当常数。

**示例:**

> M = [[ x，x，x ]
> 
> [ x，x，x]
> 
> [ x，x，x]]
> 
> 这里 M 是常数矩阵，x 是常数元素。
> 
> 以下是常数矩阵的一些例子:
> 
> A = [[ 5，5]
> 
>        [ 5, 5]]
> 
> B = [[ 12，12，12，12，12，12，12]]

*numpy* 模块中有多种方法，可以用来创建常数矩阵，如 [numpy.full()](https://www.geeksforgeeks.org/numpy-full-python/) 、[numpy . one()](https://www.geeksforgeeks.org/numpy-ones-python/)、[numpy . zeros()](https://www.geeksforgeeks.org/numpy-zeros-python/)。

### 使用 *numpy.full()* 方法

**语法:**

> numpy.full(形状，fill_value，数据类型=无，顺序= 'C ')
> 
> **参数:**
> 
> *   **形状:**行数
>     
> *   **顺序:**C _ 连片或 F _ 连片
>     
> *   **数据类型:**【可选，浮点(默认)】返回数组的数据类型。
>     
> *   **fill _ Value:**【bool，可选】数组中要填充的值。
> 
> **返回:具有给定形状、顺序和数据类型的给定常数的数组。**

**例 1:**

这里，我们将创建一个大小为 *(2，2)* (行= 2，列= 2)的常数矩阵，其常数值为 *6.3*

## 蟒蛇 3

```py
# import required module
import numpy as np

# use full() with a
# constant value of 6.3
array = np.full((2, 2), 6.3)

# display matrix
print(array)
```

**输出:**

```py
[[6.3 6.3]
 [6.3 6.3]]
```

**例 2:**

类似于上面显示的例子

## 蟒蛇 3

```py
# import required module
import numpy as np

# use full() with a
# constant value of 60
array = np.full((4, 3), 60)

# display matrix
print(array)
```