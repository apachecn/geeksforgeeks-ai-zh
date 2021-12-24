# Python | Pandas index . itemsize

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-itemsize/](https://www.geeksforgeeks.org/python-pandas-index-itemsize/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

Pandas `**Index.itemsize**`属性返回给定索引对象中基础数据项的数据类型的大小。

> **语法:** Index.itemsize
> 
> **参数:**无
> 
> **返回:**返回数据类型的大小

**示例#1:** 使用`Index.itemsize`属性找出给定索引对象中底层数据的数据类型的大小。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Melbourne', 'Sanghai', 'Lisbon', 'Doha', 'Moscow'])

# Print the index
print(idx)
```

**输出:**
![](img/72436cc2bf2e05529625f903b7e11e7d.png)

现在我们将使用`Index.itemsize`属性找出给定 Index 对象中底层数据的数据类型的大小。

```py
# return the size of dtype
result = idx.itemsize

# Print the result
print(result)
```

**输出:**
![](img/6c869ca878ed9e899dc60e57412cddcb.png)
正如我们在输出中看到的，`Index.itemsize`属性已经返回了 8，表示索引对象中底层数据的 dtype 大小为 8。

**示例 2 :** 使用`Index.itemsize`属性找出给定索引对象中底层数据的数据类型的大小。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index([900 + 3j, 700 + 25j, 620 + 10j, 388 + 44j, 900])

# Print the index
print(idx)
```

**输出:**
![](img/a9148eb763b01e778d38c820623b038c.png)

现在我们将使用`Index.itemsize`属性找出给定 Index 对象中底层数据的数据类型的大小。

```py
# return the size of dtype
result = idx.itemsize

# Print the result
print(result)
```

**输出:**
![](img/6c869ca878ed9e899dc60e57412cddcb.png)
我们在输出中可以看到，`Index.itemsize`属性已经返回了 8，表示索引对象中底层数据的 dtype 大小为 8。