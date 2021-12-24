# Python 中的 Matplotlib.pyplot.text()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-pyplot-text-function-in-python/](https://www.geeksforgeeks.org/matplotlib-pyplot-text-function-in-python/)

该函数用于将文本添加到数据坐标中 x，y 位置的轴上。

```py
Syntax: matplotlib.pyplot.text(x, y, s, fontdict=None, **kwargs)
```

<figure class="table">

| **参数** | **描述** |
| x，y:浮动 | 放置文本的位置。默认情况下，这是在数据坐标中。可以使用变换参数更改坐标系。 |
| 字符串 | 正文。 |
| fontdict : dict 默认无 | 覆盖默认文本属性的字典。如果 fontdict 为 None，则默认值由 rcParams 决定。 |
| **克瓦格斯 | 文本属性。 |

</figure>

**示例#1:** 绘图页上的文本

## python 3

```py
import matplotlib.pyplot

matplotlib.pyplot.text(0.5, 0.5, "Hello World!")
matplotlib.pyplot.savefig("out.png")
```