# 蟒蛇|熊猫 MultiIndex.levshape

> 原文:[https://www . geesforgeks . org/python-pandas-multi index-lev shape/](https://www.geeksforgeeks.org/python-pandas-multiindex-levshape/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**MultiIndex.levshape**`属性输出一个包含多索引中每个级别长度的元组。

> **语法:** MultiIndex.levshape

**示例#1:** 使用`MultiIndex.levshape`属性查找多索引中每个级别的长度。

```py
# importing pandas as pd
import pandas as pd

# Creating the array
array =[[1, 2, 3], ['Sharon', 'Nick', 'Bailey']]

# Print the array
print(array)
```

**输出:**
![](img/12ecee1bf81f73cdf3cf18dfe730920d.png)

现在让我们使用这个数组创建多索引

```py
# Creating the MultiIndex
midx = pd.MultiIndex.from_arrays(array, names =('Number', 'Names'))

# Print the MultiIndex
print(midx)
```

**输出:**
![](img/1eae73d45c2679c5ff140274d8e435ba.png)

现在我们将在多索引中找到每个级别的长度。

```py
# Print the length of each level in MultiIndex
midx.levshape
```

**输出:**
![](img/f7ba81650c4d4dfdb154d7a4591eae91.png)
正如我们在输出中看到的，midx MultiIndex 中每个级别的长度是(3，3)。

**示例 2:** 使用`MultiIndex.levshape`属性查找给定多索引中每个级别的长度。

```py
# importing pandas as pd
import pandas as pd

# Creating the array
array = [[1, 2, 3], ['Sharon', 'Nick', 'Bailey'],
                   ['Doctor', 'Scientist', 'Physicist']]

# Print the array
print(array)
```

**输出:**
![](img/aac6d50c74c2e2a467889328893e477f.png)

现在让我们使用这个数组创建多索引

```py
# Creating the MultiIndex
midx = pd.MultiIndex.from_arrays(array, names = ('Ranking', 'Names', 'Profession'))

# Print the MultiIndex
print(midx)
```

**输出:**
![](img/24ab6ffdd886b98f6d75557c194f205e.png)

现在我们将在多索引中找到每个级别的长度。

```py
# Print the length of each levels in MultiIndex
midx.levshape
```

**输出:**
![](img/d0ca088fece2c0a2f2d585ede662e8e9.png)
在输出中我们可以看到， *midx* 中每一级的长度都是 3。