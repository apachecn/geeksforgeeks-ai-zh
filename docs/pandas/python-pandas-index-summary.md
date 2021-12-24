# Python | Pandas index . summary()

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-summary/](https://www.geeksforgeeks.org/python-pandas-index-summary/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Index.summary()**`函数返回索引的汇总表示。这个函数类似于我们对数据帧的函数。

> **语法:**索引.摘要(名称=无)
> 
> **退货:**汇总

**示例#1:** 使用`Index.summary()`函数查找索引的摘要。

```
# importing pandas as pd
import pandas as pd

# Creating the index 
idx = pd.Index(['Beagle', 'Pug', 'Labrador',
                'Sephard', 'Mastiff', 'Husky'])

# Print the index
idx
```

**输出:**
![](img/19a85b26b3692341307d7ea7f2d75112.png)

现在我们将找到索引的摘要。

```
# find the summary of the Index.
idx.summary()
```

**输出:**
![](img/a1ab9b06f43d5a494305c1aa61ab0c1c.png)

正如我们在输出中看到的，该函数返回了索引的总体摘要。

**例 2:** 使用`Index.summary()`函数总结指数。

```
# importing pandas as pd
import pandas as pd

# Creating the index 
idx = pd.Index([22, 14, 8, 56, 27, 21, 51, 23])

# Print the index
idx
```

**输出:**
![](img/8935c27fda6e7f5ab189dace7a6ebfeb.png)

现在我们将找到索引的摘要。

```
# the function returns the summary of the Index
idx.summary()
```

**输出:**
![](img/f01cb0c79ce0fc55d8d90866d6f841ee.png)

正如我们在输出中看到的，该函数返回了索引的摘要。