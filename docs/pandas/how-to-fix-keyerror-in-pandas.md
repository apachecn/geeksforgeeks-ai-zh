# 如何修复:熊猫中的按键错误

> 原文:[https://www . geeksforgeeks . org/how-fix-key error in-pandas/](https://www.geeksforgeeks.org/how-to-fix-keyerror-in-pandas/)

在这篇文章中，我们将讨论如何修复熊猫的键错误。熊猫**键错误**发生在我们试图访问数据框中不存在的某个列/行标签时。通常，当您拼错列/行名称或在列/行名称之前或之后包含不需要的空格时，就会出现此错误。

使用的数据集链接在这里是

**例**

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# using .read_csv method to import dataset
df = pd.read_csv('data.csv')
```

**输出:**

![](img/bed136904cf72702dd0020478f08c891.png)

## 复制密钥错误:

## 蟒蛇 3

```py
# intentionally passing wrong spelling of
# the key present in dataset
df['country']
```

**输出:**

```py
KeyError: 'country'
```

因为没有名为“国家”的列，所以我们得到一个 KeyError。

## 如何修复密钥错误？

我们可以简单地通过纠正钥匙的拼写来纠正错误。如果我们不确定拼写，我们可以简单地打印所有列名的列表并进行交叉检查。

## 蟒蛇 3

```py
# printing all columns of the dataframe
print(df.columns.tolist())
```