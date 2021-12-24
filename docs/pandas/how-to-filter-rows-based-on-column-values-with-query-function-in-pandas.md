# 熊猫中如何用查询功能根据列值过滤行？

> 原文:[https://www . geeksforgeeks . org/如何使用熊猫查询函数基于列值筛选行/](https://www.geeksforgeeks.org/how-to-filter-rows-based-on-column-values-with-query-function-in-pandas/)

在本文中，让我们看看如何根据列值过滤行。查询函数可用于根据列值筛选行。

**考虑以下数据框:**

## 蟒蛇 3

```py
import pandas as pd

data = [['A', 10], ['B', 15], ['C', 14], ['D', 12]] 
df = pd.DataFrame(data, columns = ['Name', 'Age'])
df
```