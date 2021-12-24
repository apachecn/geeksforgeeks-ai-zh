# Python | Pandas index . hasnans

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-hasnans/](https://www.geeksforgeeks.org/python-pandas-index-hasnans/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

如果给定的索引对象中有任何缺失值，Pandas `**Index.hasnans**`属性返回`True`，否则返回`False`，表示给定的索引对象中没有缺失值。

> **语法:** Index.hasnans
> 
> **参数:**无
> 
> **返回:**布尔值

**示例#1:** 使用`Index.hasnans`属性检查给定索引对象中是否有任何缺失值。

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

现在我们将使用`Index.hasnans`属性来检查给定的 Index 对象中是否有缺失的值。

```py
# check if there is any
# missing value
result = idx.hasnans

# Print the result
print(result)
```

**输出:**

![](img/4ef10c076341ed007a036ab20b5641a3.png)

正如我们在输出中看到的那样，`Index.hasnans`属性已经返回了`False`，表明在给定的 Index 对象中没有缺失值。

**示例#2 :** 使用`Index.hasnans`属性检查给定索引对象中是否有任何缺失值。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['2012-12-12', None, '2002-1-10', None])

# Print the index
print(idx)
```

**输出:**

![](img/098934a4596cb6eb57d516f16a18cf31.png)

现在我们将使用`Index.hasnans`属性来检查给定的 Index 对象中是否有缺失的值。

```py
# check if there is any
# missing value
result = idx.hasnans

# Print the result
print(result)
```

**输出:**

![](img/b9aa5c122b77222590869ca994446661.png)

正如我们在输出中看到的那样，`Index.hasnans`属性返回了`True`，表明给定的 Index 对象中缺少一些值。