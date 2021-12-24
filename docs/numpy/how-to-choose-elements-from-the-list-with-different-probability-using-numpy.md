# 如何使用 NumPy 从不同概率的列表中选择元素？

> 原文:[https://www . geeksforgeeks . org/如何使用 numpy 从不同概率列表中选择元素/](https://www.geeksforgeeks.org/how-to-choose-elements-from-the-list-with-different-probability-using-numpy/)

我们将看到如何使用[**numpy . random . choice()**](https://www.geeksforgeeks.org/numpy-random-choice-in-python/)方法从列表中选择具有不同概率的元素。

> **语法:** numpy.random.choice(a，size=None，replace=True，p=None)
> 
> **输出:**返回随机样本的 numpy 数组。

**注意:**参数 **p** 是与(一维)数组中的每个条目相关联的概率。如果没有给出，样本假设在 **a** 中的所有条目上均匀分布。

现在，让我们看看例子:

**例 1:**

## 蟒蛇 3

```
# import numpy library
import numpy as np

# create a list
num_list = [10, 20, 30, 40, 50]

# uniformly select any element
# from the list
number = np.random.choice(num_list)

print(number)
```

**输出:**

```
50

```

**例 2:**

## 蟒蛇 3

```
# import numpy library
import numpy as np

# create a list
num_list = [10, 20, 30, 40, 50]

# choose index number-3rd element
# with 100% probability and other
# elements probability set to 0
# using p parameter of the
# choice() method so only
# 3rd index element selected
# every time in the list size of 3.
number_list = np.random.choice(num_list, 3,
                          p = [0, 0, 0, 1, 0])

print(number_list)
```

**输出:**

```
[40 40 40]

```

在上面的例子中，我们每次只想从给定的列表中选择第三个索引元素。

**例 3:**

## 蟒蛇 3

```
# import numpy library
import numpy as np

# create a list
num_list = [10, 20, 30, 40, 50]

# choose index number 2nd & 3rd element
# with  50%-50% probability and other
# elements probability set to 0
# using p parameter of the
# choice() method so 2nd & 
# 3rd index elements selected
# every time in the list size of 3.
number_list = np.random.choice(num_list, 3,
                          p = [0, 0, 0.5, 0.5, 0])

print(number_list)
```

**输出:**

```
[30 40 30]

```

在上面的例子中，我们希望每次都从给定的列表中选择第二和第三个索引元素。