# 蟒蛇|熊猫索引.大步

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-strides/](https://www.geeksforgeeks.org/python-pandas-index-strides/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

熊猫 `**Index.strides**`属性返回给定索引对象的基础数据的步长。它基本上返回一个字节数组，以便在遍历索引时单步执行每个维度。

> **语法:**索引.跨步
> 
> **参数:**无
> 
> **返回:**步数

**示例#1:** 使用`Index.strides`属性查找给定索引对象中基础数据的步长。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Melbourne', 'Sanghai', 'Lisbon', 'Doha', 'Moscow', 'Rio'])

# Print the index
print(idx)
```

**输出:**
![](img/d947b05528c70694d6702a7dceabbb1e.png)

现在我们将使用`Index.strides`属性来查找给定索引对象中底层数据的步长。

```py
# return the number of strides
result = idx.strides

# Print the result
print(result)
```

**输出:**
![](img/f66d41071f8c3e486670c3d15e416aec.png)
正如我们在输出中看到的那样，`Index.strides`属性返回了给定索引对象中底层数据的步长。

**示例 2 :** 使用`Index.strides`属性查找给定索引对象中底层数据的步长。

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

现在我们将使用`Index.strides`属性来查找给定索引对象中底层数据的步长。

```py
# return the number of strides
result = idx.strides

# Print the result
print(result)
```

**输出:**
![](img/f66d41071f8c3e486670c3d15e416aec.png)
正如我们在输出中看到的那样，`Index.strides`属性返回了给定 Index 对象中底层数据的跨度。