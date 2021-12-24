# Python |熊猫时间差指数. nlvelles

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-pandas-time delta index-nlveles/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.nlevels**`属性返回所考虑的时间增量索引对象的级别数。

> **语法:**时间增量指数. nlevels
> 
> **返回:**级别数

**示例#1:** 使用`TimedeltaIndex.nlevels`属性找出所考虑的给定时间增量索引对象的级别数

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:12.001124', periods = 5,
                                             freq ='N', name ='Koala')

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/7deceee04893841a5d10f9420bdd7b3a.png)

现在我们将找到 tidx 对象的层数。

```py
# return the number of levels of the tidx object
tidx.nlevels
```

**输出:**
![](img/f403ce1b5f286d32c53a09638e010757.png)
正如我们在输出中看到的，`TimedeltaIndex.nlevels`属性返回了 1，表示 tidx 对象的层数为 1。

**示例 2:** 使用`TimedeltaIndex.nlevels`属性找出所考虑的给定时间增量索引对象的级别数。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['-1 days 2 min 3us 10ns', '1 days 06:05:01.000030',
                                                     '-1 days + 23:59:59.999999'])

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/9fcfc935fbe07b4e4e3e3328815e648a.png)

现在我们将找到 tidx 对象的层数。

```py
# return the number of levels of the tidx object
tidx.nlevels
```

**输出:**
![](img/f403ce1b5f286d32c53a09638e010757.png)
正如我们在输出中看到的，`TimedeltaIndex.nlevels`属性返回了 1，表示 tidx 对象的层数为 1。