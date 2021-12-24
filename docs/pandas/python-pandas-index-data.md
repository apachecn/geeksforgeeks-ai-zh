# Python |熊猫索引. data

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-data/](https://www.geeksforgeeks.org/python-pandas-index-data/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

熊猫 `**Index.data**`属性返回给定索引对象的底层数据的数据指针。

> **语法:**索引.数据
> 
> **参数:**无
> 
> **返回:**内存地址

**示例#1:** 使用`Index.data`属性查找给定 Index 对象的底层数据的内存地址。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Jan', 'Feb', 'Mar', 'Apr', 'May'])

# Print the index
print(idx)
```

**输出:**

![](img/fc8b782aee16162731fbb602f61e5c2e.png)

现在我们将使用`Index.data`属性来查找给定序列对象的底层数据的内存地址。

```py
# return memory address
result = idx.data

# Print the result
print(result)
```

**输出:**

![](img/9d6a16cb5288c2da257b90ad544edc97.png)

从输出中我们可以看到，`Index.data`属性已经成功返回了给定 Index 对象的底层数据的数据指针。

**示例#2 :** 使用`Index.data`属性查找给定 Index 对象的底层数据的内存地址。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index([100, 200, 142, 88, 124])

# Print the index
print(idx)
```

**输出:**

![](img/a7e2ae3749858d771e74111e592606bd.png)

现在我们将使用`Index.data`属性来查找给定序列对象的底层数据的内存地址。

```py
# return memory address
result = idx.data

# Print the result
print(result)
```

**输出:**

![](img/098934a4596cb6eb57d516f16a18cf31.png)

从输出中我们可以看到，`Index.data`属性已经成功返回了给定 Index 对象的底层数据的数据指针。