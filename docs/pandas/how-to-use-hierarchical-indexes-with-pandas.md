# 熊猫如何使用分级索引？

> 原文:[https://www . geeksforgeeks . org/如何使用带有熊猫的分级索引/](https://www.geeksforgeeks.org/how-to-use-hierarchical-indexes-with-pandas/)

索引就像一个地址，这就是如何访问数据帧或序列中的任何数据点。行和列都有索引，行索引称为索引，而对于列，则是一般的列名。

### **分级索引**

分层索引也称为多索引，它将多个列名设置为索引。在本文中，我们将使用[无家可归. csv](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210408124122/homelessness.csv) 文件。

## 蟒 3

```py
# importing pandas library as alias pd 
import pandas as pd

# calling the pandas read_csv() function.
# and storing the result in DataFrame df
df = pd.read_csv('homelessness.csv')

print(df.head())
```