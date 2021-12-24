# Python | Pandas . to _ markdown()in Pandas

> 原文:[https://www . geesforgeks . org/python-pandas-to _ markdown-in-pandas/](https://www.geeksforgeeks.org/python-pandas-to_markdown-in-pandas/)

借助`**pandas.to_markdown()**`方法，我们可以通过使用`pandas.to_markdown()`方法从给定的数据帧中得到标记表。

> **语法:** `pandas.to_markdown()`
> 
> **返回:**返回减价表。

**示例#1 :**
在本例中，我们可以看到，通过使用`pandas.to_markdown()`方法，我们能够使用该方法从给定的数据帧中获得减价表。

```py
# import pandas
import pandas as pd

df = pd.DataFrame({"A": [1, 2, 3],
                   "B": [1.1, 2.2, 3.3]}, 
                    index =['a', 'a', 'b'])

# Using pandas.to_markdown() method
gfg = df.to_markdown()

print(gfg)
```

**输出:**

```py
|    |   A |   B |
|:---|----:|----:|
| a  |   1 | 1.1 |
| a  |   2 | 2.2 |
| b  |   3 | 3.3 |

```

**例 2 :**

```py
# import pandas
import pandas as pd

df = pd.DataFrame({"A": [3, 4, 5],
                   "B": ['c', 'd', 'e']},
                   index =['I', 'II', 'III'])

# Using pandas.to_markdown() method
gfg = df.to_markdown()

print(gfg)
```

**输出:**

```py
|     |   A | B   |
|:----|----:|:----|
| I   |   3 | c   |
| II  |   4 | d   |
| III |   5 | e   |

```