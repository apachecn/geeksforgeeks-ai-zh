# 使用 NumPy

计算相对于箱的 num 直方图

> 原文:[https://www . geeksforgeeks . org/计算使用 numpy/的面元直方图](https://www.geeksforgeeks.org/compute-the-histogram-of-nums-against-the-bins-using-numpy/)

在本文中，我们将讨论如何使用 [NumPy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 模块根据箱计算 nums。直方图是可视化数据集频率分布的最佳方式，它将数据集分割成大小相等的小区间，称为面元。 *Numpy* 直方图函数类似于 [*matplotlib*](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 库的 *hist()* 函数，唯一的区别是 Numpy 直方图给出数据集的数值表示，而 *hist()* 给出数据集的图形表示。

在创建直方图时，最好不要从箱的角度考虑，而要找出每个值出现的次数，即频率表。为此，python 字典非常适合。下面是直方图在纯 python 中的简单实现:

## python 3

```
# Dataset
a = (1, 3, 7, 7, 2, 3, 4, 7, 6, 6, 3, 5, 2)

# Creating empty dictionary
hist = {}

# Counting the number of occurrences
for i in a:
    hist[i] = hist.get(i, 0) + 1

# Printing the frequency table i.e histogram
print(hist)
```