# 如何用熊猫创建关联矩阵？

> 原文:[https://www . geeksforgeeks . org/如何使用 pandas 创建关联矩阵/](https://www.geeksforgeeks.org/how-to-create-a-correlation-matrix-using-pandas/)

**相关性**是一种显示两个变量如何相关的统计技术。[利用熊猫数据框法建立相关矩阵。它用于查找数据框中所有列的成对相关性。任何 na 值都会被自动排除。对于 dataframe 中的任何非数字数据类型列，它都将被忽略。
**要使用熊猫创建相关矩阵，应采取以下步骤:**](https://www.geeksforgeeks.org/python-pandas-dataframe-corr/) 

1.  获取数据。
2.  使用熊猫创建数据帧。
3.  使用熊猫创建相关矩阵

**例 1:**

## 蟒蛇 3

```
# import pandas
import pandas as pd

# obtaining the data
data = {'A': [45, 37, 42],
        'B': [38, 31, 26],
        'C': [10, 15, 17]
        }
# creation of DataFrame
df = pd.DataFrame(data)

# creation of correlation matrix
corrM = df.corr()

corrM
```