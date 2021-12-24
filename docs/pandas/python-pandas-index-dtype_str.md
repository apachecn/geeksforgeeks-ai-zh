# python | panda index . dttype _ str

> 原文:[https://www . geesforgeks . org/python-pandas-index-dtype _ str/](https://www.geeksforgeeks.org/python-pandas-index-dtype_str/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

Pandas `**Index.dtype_str**`属性以字符串形式返回给定索引对象的基础数据的数据类型(dtype)。

> **语法:** Index.dtype_str
> 
> **参数:**无
> 
> **以字符串形式返回:**数据类型

**示例#1:** 使用`Index.dtype_str`属性以字符串形式查找给定索引对象的基础数据的数据类型。

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

现在我们将使用`Index.dtype_str`属性以字符串的形式查找给定序列对象的底层数据的数据类型。

```py
# return the dtype as a string
result = idx.dtype_str

# Print the result
print(result)
```

**输出:**

![](img/0f20cfe846d283d1fb51915dc8491911.png)

正如我们在输出中看到的那样，`Index.dtype_str`属性已经以字符串的形式返回了给定 Index 对象的底层数据的数据。

**示例#2 :** 使用`Index.dtype_str`属性以字符串形式查找给定索引对象的基础数据的数据类型。

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

现在我们将使用`Index.dtype_str`属性以字符串的形式查找给定序列对象的底层数据的数据类型。

```py
# return the dtype as a string
result = idx.dtype_str

# Print the result
print(result)
```

**输出:**

![](img/098934a4596cb6eb57d516f16a18cf31.png)

正如我们在输出中看到的那样，`Index.dtype_str`属性已经以字符串的形式返回了给定 Index 对象的底层数据的数据。