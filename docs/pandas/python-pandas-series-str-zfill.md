# Python | Pandas series . str . zfill()

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-z fill/](https://www.geeksforgeeks.org/python-pandas-series-str-zfill/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **`zfill()`** 方法是用零填充字符串的左侧。如果字符串的长度大于或等于宽度参数，则没有零作为前缀。由于这是一种弦法，所以只适用于系列弦和 ***。str*** 每次调用这个方法之前都要加上前缀。

**用法:**每当处理以字符串格式存储的数值数据时，都可以使用该功能。例如，如果一个序列包含不同位大小的二进制数。然后，为了进行类似 1 补数加法的运算，每个二进制都需要具有相同的位大小。

> **语法:** Series.str.zfill(宽度)
> 
> **参数:**
> **宽度:**前置零后输出字符串的最大宽度。
> 
> **返回类型:**前缀为 0 的序列。

要下载以下示例中使用的数据集，请单击此处的[。](https://media.geeksforgeeks.org/wp-content/uploads/employees.csv)

在以下示例中，使用的数据框包含一些员工的数据。任何操作前的数据框图像附在下面。
![](img/aa19a387661521c5966c77c214eb5188.png)

**示例:**在薪资列前加零。

在本例中，使用`zfill()`方法设置 8 的宽度，并在“薪资”列前加零。由于薪资列的数据类型为 int64，因此首先使用 astype()方法将其转换为字符串。

```
# importing pandas 
import pandas as pd 

# making data frame from csv at url 
data = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/employees.csv") 

# converting to string dtype
data["Salary"]= data["Salary"].astype(str)

# width of output string
width = 10

# calling method and overwriting series
data["Salary"]= data["Salary"].str.zfill(width)

# display
data
```

**输出:**
如输出图所示，前面加了零，现在薪资列中每个字符串的长度都是 10。
![](img/16f8714ff9ba48066968cf42eafd60b7.png)