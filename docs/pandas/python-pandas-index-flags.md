# Python |熊猫索引. flags

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-flags/](https://www.geeksforgeeks.org/python-pandas-index-flags/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

熊猫 `**Index.flags**`属性返回给定索引对象的所有标志的状态。

> **语法:**索引.标志
> 
> **参数:**无
> 
> **返回:**标志状态

**示例#1:** 使用`Index.flags`属性查找给定索引对象的所有标志的状态。

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

现在我们将使用`Index.flags`属性来查找给定索引对象的所有标志的状态。

```py
# return the status of the flags
result = idx.flags

# Print the result
print(result)
```

**输出:**

![](img/180444971798094d798e9425084ead01.png)

正如我们在输出中看到的那样，`Index.flags`属性返回了给定索引对象的所有标志的状态。

**示例#2 :** 使用`Index.flags`属性查找给定索引对象的所有标志的状态。

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

现在我们将使用`Index.flags`属性来查找给定索引对象的所有标志的状态。

```py
# return the status of the flags
result = idx.flags

# Print the result
print(result)
```

**输出:**

![](img/180444971798094d798e9425084ead01.png)

正如我们在输出中看到的那样，`Index.flags`属性返回了给定索引对象的所有标志的状态。