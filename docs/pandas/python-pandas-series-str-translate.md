# Python | Pandas series . str . translate()

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-translate/](https://www.geeksforgeeks.org/python-pandas-series-str-translate/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **`str.translate()`** 是最重要也是最复杂的串法之一。它使用翻译表根据翻译表翻译调用者的字符串序列。如果要翻译的值不止一个，字典会传递给[maktrans 函数](https://www.geeksforgeeks.org/python-maketrans-translate-functions/)来创建翻译表。

> **语法:** Series.str.translate(table，deletechars=None)
> 
> **参数:**
> **表:**由 Python3 中的字典和 Python2 中的列表组成的翻译表。
> **删除字符:**字符串类型，要删除的字符。此参数仅在 Python2 中正常工作(直到熊猫版本 0.23)
> 
> **返回类型:**一系列带翻译值的字符串

要下载下例使用的数据集，点击这里的[。](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)

在下面的例子中，使用的数据框包含了一些 NBA 球员的数据。任何操作前的数据框图像附在下面。
![](img/793ad040c852f46d3cbfdaf19ee388c2.png)

**示例#1:**
在本例中，通过字典创建翻译表。字典以 a、b 和 c 为键，X、Y 和 Z 分别为值。创建转换表，分别用 X、Y 和 Z 替换 a、b 和 c。此表被传递给 str.translate()方法以进行相应的更改。

```py
# importing pandas module 
import pandas as pd

# reading csv file from url 
data = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/nba.csv")

# dropping null value columns to avoid errors
data.dropna(inplace = True)

# creating dictionary for trans table
trans_dict ={"a": "X", "b": "Y", "c": "Z"}

# creating translate table from dictionary
trans_table ="abc".maketrans(trans_dict)

# translating through passed transtable
data["Name"]= data["Name"].str.translate(trans_table)

# display
data
```

**输出:**
如输出图片所示，更改成功，字母替换成功。
![](img/85c38352ffe0c24de3e07d968566ceae.png)