# 蟒蛇|熊猫索引. size

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-size/](https://www.geeksforgeeks.org/python-pandas-index-size/)

熊猫索引是一个实现有序的、可切片的集合的不可变数组。它是存储所有熊猫对象的轴标签的基本对象。

Pandas `**Index.size**`属性返回给定索引对象的基础数据中的元素数量。

> **语法:**索引.大小
> 
> **参数:**无
> 
> **返回:**索引中的元素数量

**示例#1:** 使用`Index.size`属性查找给定索引对象的基础数据中的元素数量。

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

现在我们将使用`Index.size`属性来查找给定 Index 对象中的元素数量。

```py
# return the number of elements
result = idx.size

# Print the result
print(result)
```

**输出:**
![](img/1fb253909dab24290355ff1c54deec98.png)
正如我们在输出中看到的，`Index.size`属性已经返回了给定 Index 对象中的元素数量。

**示例 2 :** 使用`Index.size`属性查找给定 Index 对象的底层数据中的元素数量。

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

现在我们将使用`Index.size`属性来查找给定 Index 对象中的元素数量。

```py
# return the number of elements
result = idx.size

# Print the result
print(result)
```

**输出:**
![](img/d64bc442f9b07515893f28d570987f72.png)
正如我们在输出中看到的，`Index.size`属性已经返回了给定 Index 对象中的元素数量。