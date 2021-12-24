# 蟒蛇|熊猫索引.推断 _ 类型

> 原文:[https://www . geesforgeks . org/python-pandas-index-explicated _ type/](https://www.geeksforgeeks.org/python-pandas-index-inferred_type/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

Pandas `**Index.inferred_type**`属性返回从给定索引对象的值推断出的数据类型的字符串。

> **语法:**索引.推断 _ 类型
> 
> **参数:**无
> 
> **返回:**推断 _ 类型

**示例#1:** 使用`Index.inferred_type`属性找出给定索引对象中值的推断数据类型。

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Jan', 'Feb', 'Mar', 'Apr', 'May'])

# Print the index
print(idx)
```

**输出:**

```
Index(['Jan', 'Feb', 'Mar', 'Apr', 'May'], dtype='object')

```

现在我们将使用`Index.inferred_type`属性找出给定索引对象的底层数据的推断数据类型。

```
# return the inferred dtype
result = idx.inferred_type

# Print the result
print(result)
```

**输出:**

```
mixed
```

正如我们在输出中看到的那样，`Index.inferred_type`属性已经返回了`String`作为给定 Index 对象的推断数据类型。

**示例#2 :** 使用`Index.inferred_type`属性找出给定索引对象中值的推断数据类型。

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['2012-12-12', None, '2002-1-10', None])

# Print the index
print(idx)
```

**输出:**

```
Index(['2012-12-12', None, '2002-1-10', None], dtype='object')
```

现在我们将使用`Index.inferred_type`属性找出给定索引对象的底层数据的推断数据类型。

```
# return the inferred dtype
result = idx.inferred_type

# Print the result
print(result)
```

**输出:**

```
mixed
```

正如我们在输出中看到的那样，`Index.inferred_type`属性已经返回了`mixed`作为给定 Index 对象的推断数据类型。