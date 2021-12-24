# Python | Pandas data frame . to _ latex()方法

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-to _ latex-method/](https://www.geeksforgeeks.org/python-pandas-dataframe-to_latex-method/)

借助`**DataFrame.to_latex()**`方法，我们可以得到 latex 文档形式的数据帧，我们可以使用`DataFrame.to_latex()`方法将其作为单独的文件打开。

> **语法:** `DataFrame.to_latex()`
> **返回:**将数据帧作为乳胶文档返回。

**示例#1 :**
在这个示例中，我们可以说通过使用`DataFrame.to_latex()`方法，我们能够获得 latex 文档形式的数据帧。

```
# import DataFrame
import pandas as pd

# using DataFrame.to_latex() method
gfg = pd.DataFrame({'Name': ['Marks'], 
                    'Jitender': ['78'],
                    'Rahul': ['77.9']})

print(gfg.to_latex(index = True, multirow = True))
```

**输出:**

> \ begin { table } { llll }
> \ toprule
> { }&名称&Jitender&Rahul \ \
> \ mid rule
> 0&标记&78&77.9 \ \
> \ bottom rule
> \ end { table }

**例 2 :**

```
# import DataFrame
import pandas as pd

# using DataFrame.to_latex() method
gfg = pd.DataFrame({'Name': ['Marks', 'Gender'],
                    'Jitender': ['78', 'Male'], 
                    'Purnima': ['78.9', 'Female']})

print(gfg.to_latex(index = False, multirow = True))
```

**输出:**

> \ begin { table } { lll }
> \ toprule
> 姓名&吉坦德&普尼玛\\
> \midrule
> 标记& 78 & 78.9 \\
> 性别&男&女\ \
> \ bottom rule
> \ end { table }