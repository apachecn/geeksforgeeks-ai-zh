# 获取两个熊猫系列不常见的物品

> 原文:[https://www . geeksforgeeks . org/get-the-items-非-common-of-two-pandas-series/](https://www.geeksforgeeks.org/get-the-items-which-are-not-common-of-two-pandas-series/)

Pandas 不支持执行集合操作的特定方法。但是，我们可以使用以下公式从这两个集合中获取唯一的项目:

![  A \cup  B - (A \cap B)  ](img/aea12f4a0353c9e4431e7042b4563bcd.png "Rendered by QuickLaTeX.com")

**算法:**

1.  导入`Pandas` 和`NumPy` 模块。
2.  创建 2 `Pandas Series`。
3.  使用`union1d()`方法求数列的并集。
4.  用`intersect1d()`方法求数列的交点。
5.  找出并集和交集元素之间的区别。使用`isin()`方法获取“并集”和“交集”中出现的项目的布尔列表。
6.  打印结果

```py
# import the modules
import pandas as pd 
import numpy as np

# create the series 
ser1 = pd.Series([1, 2, 3, 4, 5])
ser2 = pd.Series([3, 4, 5, 6, 7])

# union of the series
union = pd.Series(np.union1d(ser1, ser2))

# intersection of the series
intersect = pd.Series(np.intersect1d(ser1, ser2))

# uncommon elements in both the series 
notcommonseries = union[~union.isin(intersect)]

# displaying the result
print(notcommonseries)
```

**输出:**

```py
1, 2, 6, 7
```