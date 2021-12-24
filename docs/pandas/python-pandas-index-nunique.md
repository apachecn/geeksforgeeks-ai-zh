# python | panda index . nuneme()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python 熊猫索引-nuneme/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Index.nunique()**`函数返回对象中唯一元素的个数。它返回一个标量值，该值是索引中所有唯一值的计数。默认情况下，`NaN`值不包括在计数中。如果 dropna 参数被设置为`False`，则它在计数中包括`NaN`值。

> **语法:**index . never(drop na = true)
> 
> **参数:**
> **dropna :** 不要把 NaN 算在内。
> 
> **返回:**努尼克:int

**示例#1:** 使用`Index.nunique()()`函数查找索引中唯一值的计数。计数中不包括`NaN`值。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Beagle', 'Pug', 'Labrador', 'Pug',
                        'Mastiff', None, 'Beagle'])

# Print the Index
idx
```

**输出:**
![](img/d22dd1c64903fcf159a69225e8e1f7c9.png)

让我们找出索引中唯一值的计数。

```py
# to find the count of unique values.
idx.nunique(dropna = True)
```

**输出:**
![](img/222a5346c7f24d3ef7f61f97c61066d7.png)
正如我们在输出中看到的，函数返回了 4，表明 Index 中只有 4 个唯一值。

**例 2:** 使用`Index.nunique()`函数找出索引中所有唯一的值。也包括计数中的缺失值，即`NaN`值。

```py
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Beagle', 'Pug', 'Labrador', 'Pug',
                        'Mastiff', None, 'Beagle'])

# Print the Index
idx
```

**输出:**
![](img/d22dd1c64903fcf159a69225e8e1f7c9.png)

让我们找出索引中唯一值的计数。

```py
# to find the count of unique values.
idx.nunique(dropna = False)
```

**输出:**
![](img/65366cbc9959ce0eac1e5c0b72cf9427.png)
正如我们在输出中看到的，函数返回了 5，表示 Index 中只有 5 个唯一值。我们还在计数中包括了缺失的值。