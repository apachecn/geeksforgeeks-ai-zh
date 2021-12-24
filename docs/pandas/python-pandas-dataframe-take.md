# Python | Pandas data frame . take()

> 原文:[https://www.geeksforgeeks.org/python-pandas-dataframe-take/](https://www.geeksforgeeks.org/python-pandas-dataframe-take/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**dataframe.take()**`函数返回给定位置索引中沿轴的元素。这意味着我们不是根据对象的索引属性中的实际值进行索引。我们根据元素在对象中的实际位置进行索引。

> **语法:**数据帧获取(索引，轴=0，转换=无，is _ copy =真，**kwargs)
> 
> **参数:**
> **指数:**一组指示采取哪些立场的整数。
> **轴:**选择元素的轴。0 表示我们正在选择行，1 表示我们正在选择列
> **转换:**是否将负指数转换为正指数。例如，-1 将映射到镜头(轴)–1。这些转换类似于索引常规 Python 列表的行为。
> **is_copy :** 是否返回原对象的副本。
> ****kwargs :** 与 numpy.take()兼容。对输出没有影响。
> 
> **返回:**一个类似数组的数组，包含从对象中获取的元素。

有关代码中使用的 CSV 文件的链接，请单击此处的

**示例#1:** 使用`take()`函数获取索引轴上的一些值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe 
df = pd.read_csv("nba.csv")

# Print the dataframe
df
```

![](img/43dab26aa0d03954ff5c64000900287e.png)

现在，出于演示目的，我们将修改索引标签。现在标签的编号是从 0 到 914。

```py
# double the value of index labels
df.index = df.index * 2

# Print the modified dataframe
df
```

![](img/2039f0f5c69bc9a312ed385f933e7cd2.png)

让我们取位置 0、1 和 2 的值

```py
# take values at input position over the index axis

df.take([0, 1, 2], axis = 0)
```

**输出:**
![](img/cf2fcd37b2324e85f24779d0cbdd4f91.png)
正如我们在输出中看到的，值是根据位置而不是索引标签选择的。

**示例#2:** 使用`take()`函数获取列轴上位置 0、1 和 2 的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe 
df = pd.read_csv("nba.csv")

# Print the dataframe
df
```

![](img/43dab26aa0d03954ff5c64000900287e.png)

现在我们将取列轴上位置 0、1 和 2 的值。

```py
# take values over the column axis.

df.take([0, 1, 2], axis = 1)
```

**输出:**
![](img/494f2e6c5079375796a2bce390d0440c.png)