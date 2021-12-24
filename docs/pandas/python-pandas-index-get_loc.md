# Python | Pandas index . get _ loc()

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-get_loc/](https://www.geeksforgeeks.org/python-pandas-index-get_loc/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**Index.get_loc()**`函数为请求的标签返回整数位置、切片或布尔掩码。该函数既可以处理排序索引，也可以处理未排序索引。如果传递的值不在索引中，它会提供各种选项。只有在对索引标签进行排序时，您才可以选择将前一个值或下一个值返回到传递的值。

> **语法:** Index.get_loc(键，方法=无，容差=无)
> 
> **参数:**
> **键:**标注
> **方法:** {None、' pad'/'ffill '、'回填'/'bfill '、'最近' }，可选
> **- >** **默认:**仅精确匹配。
> **->****pad/ffill:**如果没有精确匹配，则查找 PREVIOUS 索引值。
> **- >** **回填/填充:**如果没有精确匹配，则使用 NEXT 索引值
> **- >** **如果没有精确匹配，则使用 NEXTERAL 索引值。通过选择较大的索引值来打破并列距离。**
> 
> **返回:** loc:如果唯一索引，则为 int，如果单调索引，则为 slice，否则为 mask

**示例#1:** 使用`Index.get_loc()`函数查找传递值的位置。

```
# importing pandas as pd
import pandas as pd

# Creating the Index
idx = pd.Index(['Labrador', 'Beagle', 'Labrador',
                     'Lhasa', 'Husky', 'Beagle'])

# Print the Index
idx
```

**输出:**
![](img/eb7ad3c04b88b01d883901e012226b90.png)

让我们找出“拉萨”在索引中的位置。

```
# Print the location of the passed value..
idx.get_loc('Lhasa)
```

**输出:**
![](img/292973aaa0b44fe5c3626bce548bb345.png)
正如我们在输出中看到的，`Index.get_loc()`函数返回了 3，表示传递的值出现在索引中的这个位置。

**例 2:** 使用`Index.get_loc()`函数查找传递值的位置。如果传递的值不在索引中，则返回刚好小于传递值的前一个值的位置。

```
# importing pandas as pd
import pandas as pd

# Creating the Index
idx = pd.Index([1, 2, 3, 14, 25, 37, 48, 69, 100])

# Print the Index
idx
```

**输出:**
![](img/e2765b79b95e7ff9136dc780bcb7577f.png)

让我们找到值 33 在索引中的位置。

```
# Find the position of 33 in the index.
# If it is not present then we forward 
# fill and return the position of previous value.
idx.get_loc(33, method ='ffill')
```

**输出:**
![](img/bfae25994a662a1b240970b23dced4a3.png)

如我们所见，该函数返回了输出 3。由于索引中不存在 33，但在排序顺序中，略小于 33 的值为 25，其位置为 4。所以，输出是 4。如果我们不设置方法参数，那么如果值不存在，就会导致错误。