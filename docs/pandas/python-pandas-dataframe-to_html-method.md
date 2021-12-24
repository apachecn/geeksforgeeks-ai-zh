# Python | Pandas data frame . to _ html()方法

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-to _ html-method/](https://www.geeksforgeeks.org/python-pandas-dataframe-to_html-method/)

借助`**DataFrame.to_html()**`方法，我们可以用`DataFrame.to_html()`方法得到一个数据帧的 html 格式。

> **语法:** `DataFrame.to_html()`
> **返回:**返回数据帧的 html 格式。

**示例#1 :**
在这个示例中，我们可以说通过使用`DataFrame.to_html()`方法，我们能够获得数据帧的 html 格式。

```py
# import DataFrame
import pandas as pd

# using DataFrame.to_html() method
gfg = pd.DataFrame({'Name': ['Marks'], 
                    'Jitender': ['78'],
                    'Rahul': ['77.9']})

print(gfg.to_html())
```

**输出:**

> |  | 名称 | 吉腾德 | 拉胡尔 |
> | --- | --- | --- | --- |
> | 0 | 标记 | 78 | 77.9 |

**例 2 :**

```py
# import DataFrame
import pandas as pd

# using DataFrame.to_html() method
gfg = pd.DataFrame({'Name': ['Marks', 'Gender'],
                    'Jitender': ['78', 'Male'],
                    'Purnima': ['78.9', 'Female']})

print(gfg.to_html())
```

**输出:**

> |  | 名 | 吉坦德 | 普尼玛 |
> | --- | --- | --- | --- |
> | 0 | 马克 | 78 | 78.9 |
> | 1 | 性别 | 男 | 女 |