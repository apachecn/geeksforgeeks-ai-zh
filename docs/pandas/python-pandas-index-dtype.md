# 蟒蛇|熊猫索引. dtype

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-dtype/](https://www.geeksforgeeks.org/python-pandas-index-dtype/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

熊猫 `**Index.dtype**`属性返回给定索引对象的基础数据的数据类型(数据类型)。

> **语法:**索引.数据类型
> 
> **参数:**无
> 
> **返回:**数据类型

**示例#1:** 使用`Index.dtype`属性查找给定索引对象的底层数据的数据类型。

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Jan', 'Feb', 'Mar', 'Apr', 'May'])

# Print the index
print(idx)
```

**输出:**

![](img/fc8b782aee16162731fbb602f61e5c2e.png)

现在我们将使用`Index.dtype`属性来查找给定序列对象的底层数据的数据类型。

```
# return the dtype
result = idx.dtype

# Print the result
print(result)
```

**输出:**

![](img/0f861ba3d9752212fea1fb7ce2355566.png)

正如我们在输出中看到的那样，`Index.dtype`属性已经返回了`object`作为给定 Index 对象的底层数据的数据类型。

**示例#2 :** 使用`Index.dtype`属性查找给定索引对象的底层数据的数据类型。

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index([100, 200, 142, 88, 124])

# Print the index
print(idx)
```

**输出:**

![](img/a7e2ae3749858d771e74111e592606bd.png)

现在我们将使用`Index.dtype`属性来查找给定序列对象的底层数据的数据类型。

```
# return the dtype
result = idx.dtype

# Print the result
print(result)
```

**输出:**

![](img/098934a4596cb6eb57d516f16a18cf31.png)

正如我们在输出中看到的那样，`Index.dtype`属性已经返回了`int64`作为给定 Index 对象的底层数据的数据类型。