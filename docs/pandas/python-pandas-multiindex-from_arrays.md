# Python | Pandas multi index . from _ arrays()

> 原文:[https://www . geesforgeks . org/python-pandas-multi index-from _ arrays/](https://www.geeksforgeeks.org/python-pandas-multiindex-from_arrays/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**MultiIndex.from_arrays()**`函数用于将数组转换为 MultiIndex。这是我们构建多索引的几种方法之一。

> **语法:**multi index . from _ arrays(arrays，sortorder=None，names = None)
> 
> **参数:**
> **数组:**每个类数组给每个数据点一个级别的值。len(arrays)是级别数
> **排序顺序:**排序级别(必须按该级别按字典顺序排序)
> 
> **返回:**索引:多索引

**示例#1:** 使用`MultiIndex.from_arrays()`函数从数组构建多索引。

```
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

```
# Creating the MultiIndex
midx = pd.MultiIndex.from_arrays(array,
            names =('Number', 'Names'))

# Print the MultiIndex
print(midx)
```

**输出:**
![](img/1eae73d45c2679c5ff140274d8e435ba.png)
正如我们在输出中看到的，该函数已经使用数组创建了一个 MultiIndex 对象。

**示例 2:** 使用`MultiIndex.from_arrays()`函数从数组中构建多索引。

```
# importing pandas as pd
import pandas as pd

# Creating the array
array =[[1, 2, 3], ['Sharon', 'Nick', 'Bailey'], 
          ['Doctor', 'Scientist', 'Physicist']]

# Print the array
print(array)
```

**输出:**
![](img/aac6d50c74c2e2a467889328893e477f.png)

现在让我们使用这个数组创建多索引

```
# Creating the MultiIndex
midx = pd.MultiIndex.from_arrays(array, 
   names =('Ranking', 'Names', 'Profession'))

# Print the MultiIndex
print(midx)
```

**输出:**
![](img/24ab6ffdd886b98f6d75557c194f205e.png)
正如我们在输出中看到的，函数已经使用传递的数组创建了一个 MultiIndex。