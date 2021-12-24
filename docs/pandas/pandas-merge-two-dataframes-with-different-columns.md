# 熊猫–合并两个不同列的数据框

> 原文:[https://www . geesforgeks . org/pandas-merge-two-data frames-with-differential-columns/](https://www.geeksforgeeks.org/pandas-merge-two-dataframes-with-different-columns/)

*熊猫*支持三种数据结构。它们是系列、数据框和面板。一个**数据框**是一个二维的数据结构，这里的数据是以表格的形式存储的，表格分为行和列。我们可以通过多种方式创建数据框。

这里我们使用 python 中的列表数据结构创建一个数据框。

## 蟒 3

```
# import required module
import pandas

# assign data
l=["vignan","it","sravan","subbarao"]

# create data frame
df = pandas.DataFrame(l)

# display dataframe
df
```