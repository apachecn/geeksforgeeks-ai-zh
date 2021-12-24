# Python |熊猫系列。nuneme()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫系列-nuneme/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

在分析数据时，很多时候用户希望看到特定列中的唯一值。熊猫 **`nunique()`** 用来计算独特的价值。

要下载使用的 CSV 文件，点击[这里](https://media.geeksforgeeks.org/wp-content/uploads/employees.csv)。

> **语法:**系列。永不(dropna=True)
> 
> **参数:**
> **dropna:** 如果为真，则排除空值
> 
> **返回类型:**整数–一列中唯一值的数量。

**示例#1:** 使用 nunique()
在本例中，nunique()方法用于获取 Team 列中所有唯一值的数量。

```
# importing pandas package
import pandas as pd

# making data frame from csv file
data = pd.read_csv("employees.csv")

# storing unique value in a variable
unique_value = data["Team"].nunique()

# printing value
print(unique_value)
```

**输出:**
返回唯一值个数的输出。

```
10
```

**示例#2:** 空值处理
在此示例中，将 unique()方法返回的数组长度与 nunique()方法返回的整数进行比较。

```
# importing pandas package
import pandas as pd

# making data frame from csv file
data = pd.read_csv("employees.csv")

# storing unique value in a variable
arr = data["Team"].unique()

# storing unique value in a variable
unique_value = data["Team"].nunique(dropna = True)

# printing values
print(len(arr), unique_value)
```

**输出:**
两种情况下的输出都不相同，因为 dropna 参数设置为真，因此在计算唯一值时排除了空值。

```
11 10
```